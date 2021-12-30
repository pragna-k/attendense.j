# attendense.j
import  java.util.Scanner;
interface student
{
void getvalue();
}
interface department
{
void getattendense();
}
class exam implements student,department
{
int sno;
String sname,class_n;
int attendense;
Scanner inp=new Scanner(System.in);
public void getvalue()
{
System.out.println("enter student name");
sname=inp.nextLine();
System.out.println("enter class:");
class_n=inp.nextLine();
System.out.println("enter student number");
sno=inp.nextInt();
}
public void getattendense()
{
System.out.println("enter student attendense");
attendense=inp.nextInt();
}
void calattendense()
{
System.out.println("student name"+sname);
System.out.println("class is"+class_n);
System.out.println("student number:"+sno);
System.out.println("student attendense:"+attendense);
}
void booleligible()
{
if(attendense>75)
{
System.out.println("True");
}
else
{
System.out.println("False");
}
}
}
class attendense
{
public static void main(String args[])
{
int i,m;
Scanner inp=new Scanner(System.in);
System.out.println("enter no.of students");
m=inp.nextInt();
exam e[]=new exam[m];
for(i=0;i<m;i++)
{
System.out.println("details of student"+(i+1));
e[i]=new exam();
e[i].getvalue();
e[i].getattendense();
e[i].calattendense();
e[i].booleligible();
}
}
}
