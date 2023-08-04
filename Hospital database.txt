7.	Design a C++ program for a hospital to create a databaseregarding its indoor patients. (Identify the member function).create a base class to store above 
information, member functionshould include functions to enter information and display list ofall the patients in the database. Create a derived class to 
storetheinformationaboutpaediatricpatients(lessthan12yrsage).
#include <iostream>usingnamespacestd;
structdate
{
int d;int m;inty;
};

classhospital
{
char name[100];struct date d_adm;structdated_dis;
protected:int age;public:
voidgetdata()
{
cout<<"Enter name of the patient: ";cin>>name;
cout<<"Enter age: ";cin>>age;
cout<<"Enter date of admission: ";cin>>d_adm.d>>d_adm.m>>d_adm.y;cout<<"Enter date of discharge: ";cin>>d_dis.d>>d_dis.m>>d_dis.y;
}
voiddisplay()
{
cout<<name<<"\t";cout<<age<<"\t";
cout<<d_adm.d<<'-'<<d_adm.m<<'-'<<d_adm.y<<"\t \t";cout<<d_dis.d<<'-'<<d_dis.m<<'-'<<d_dis.y;
}
};

classpediatric_patient:publichospital
{
char vaccine[20];public:
voidget()
{
getdata();
cout<<"enter the name of vaccine to be given \n";cin>>vaccine;
}
 
voidput()
{
if(age<12)
{
display();cout<<"\t"<<"\t";cout<<vaccine;cout<<"\n";

 
}
else

}
};
 


cout<<"agegreaterthan12notapediatricpatient";
 
intmain()
{
hospital h[5];intn;
cout<<"Enter the number of patients \n";cin>>n;
for(inti=0;i<n;i++)
{
h[i].getdata();
}
cout<<"Patientdatabase\n";
cout<<"NAME"<<"\t"<<"AGE"<<"\t"<<"DATE_OF_ADMISSION"<<"\t"
<<"DATE_OF_DISCHARGE\n";
for(inti=0;i<n;i++)
{
h[i].display();cout<<"\n";

}
pediatric_patienta1[5];
cout<<"Enter the number of pediatric patients \n";cin>>n;
for(inti=0;i<n;i++)
{
a1[i].get();

}
cout<<"pediatricPatientdatabase\n";
cout<<"NAME"<<"\t"<<"AGE"<<"\t"<<"DATE_OF_ADMISSION"<<"\t"
<<"DATE_OF_DISCHARGE"<<"\t"<<"VACCINE\n";
for(inti=0;i<n;i++)
{
a1[i].put();
}
return0;
