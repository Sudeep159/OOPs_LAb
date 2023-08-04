Designa C++ program to keep the track of the number of objects of a particular class type that are inexistence using a staticvariable.
#include <iostream>usingnamespacestd;
classCounter
{
  public:
  static int count;
  Counter()
  {
    count++;
  }
  ~Counter()
  {
    count--;
  }
};

int Counter::count;
voidf();
intmain(void)
{
  Countero1;
  cout <<"Objects in existence: ";
  cout << Counter::count <<"\n";
  Countero2;
  cout <<"Objects in existence: ";
  cout << Counter::count <<"\n";
  f();
  cout <<"Objects in existence: ";
  cout << Counter::count <<"\n";
  return0;
}

voidf()
{
  Countertemp;
  cout <<"Objects in existence: ";
  cout<<Counter::count<<"\n";
}
