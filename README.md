# SE_OOP-assignment--3                [Design and develop inheritance for a given case study, identify objects and relationships and implement
                                     inheritance wherever applicable. Employee class hasEmp_name, Emp_id, Address,Mail_id, and Mobile_nos
                                     members. Inherit the classes: Programmer, Team Lead, Assistant Project Manager and Project Manager from
                                        employee class. Add Basic Pay (BP) as the member of all the inherited classes with 97% of BP as DA, 10 % of
                                     BP as HRA, 12% of BP as PF, 0.1% of BP for staff club fund. Generate pay slips for the employees with their
                                     gross and net salary]





class Employee {
String name, add, mail;
int mobile;
float id, basic;
void salary() {
float da, hra, pf, cf, gross;
da = 97/100*basic;
hra = 10/100*basic;
pf = 12/100*basic;
cf = basic*0.1f/100;
gross = basic + da + hra - pf - cf;
System.out.println("Name:" + name);
System.out.println("Address:"+add);
System.out.println("E_mail:"+ mail);
System.out.println("Mobile:"+mobile);
System.out.println("Emp_id:"+id);
System.out.println("Basic salary:" + basic);
System.out.println("Gross salary:" + gross);
}
}
class ProMan extends Employee {
ProMan(String name, String add, String mail,int mobile,float id,int sal) {
System.out.println("--Project Manager Salary Slip--");
this.name = name;
this.add=add;
this.mail=mail;
this.mobile=mobile;
this.id=id;
basic = sal;
}
}
class APM extends Employee {
APM(String name, String add, String mail,int mobile,float id,int sal){
System.out.println("--Assistant Project Manager Salary Slip--");
this.name = name;
this.add=add;
this.mail=mail;
this.mobile=mobile;
this.id=id;
basic = sal;
}
}
class TeamLead extends Employee
TeamLead(String name, String add, String mail,int mobile,float id,int sal) {
System.out.println("--Team Leader Salary Slip--");
this.name = name;
this.add=add;
this.mail=mail;
this.mobile=mobile;
this.id=id;
basic = sal;
}
}
class programmer extends Employee {
programmer(String name, String add, String mail,int mobile,float id,int sal) {
System.out.println("--Programmer Salary Slip--");
this.name = name;
this.add=add;
this.mail=mail;
this.mobile=mobile;
this.id=id;
basic = sal;
}
}
class Inheritance{
public static void main(String[] args) {
ProMan p=new ProMan("Aman Kale","Pune","asd@gmail.com",1234567891,101,60000);
p.salary();
APM a=new APM("Amar Date","Pune","ertd@gmail.com",321456987,102,50000);
a.salary();
TeamLead t=new TeamLead("Ram Rane","Mumbai","trya23@gmail.com",456789123,104,45000);
t.salary();
programmer r=new programmer("Radha Mane","Mumbai","yugfc67@gmail.com",894561236,104,55000);
r.salary();
}
}
