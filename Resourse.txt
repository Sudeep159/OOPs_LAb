Design a C++ program to implement access control to someshared resource used by all objects of a class using a staticvariable
#include<iostream>
using namespace std;
class resource
{
  static int res;
  public:
  static int getr();
  voidfree_res()
  {
    res=0;
  }
};
int resource::res;
intresource::getr()
{
  if(res)
    return0;
  else
  {
    res=1;
    return1;
  }
}
int main()
{
  resource a,b;if(resource::getr())
  cout<<"Resource under use, object a is using \n";if(!resource::getr())
  cout<<"Resource busy, object b access denied \n";a.free_res();
  if(resource::getr())
  cout<<"Resource can now be used by Object b \n";
  return0;
}
