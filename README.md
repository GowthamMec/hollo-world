import java.util.Scanner;

class Details   
{
	protected String name;
	protected int age;
	protected String gender;
	
	Scanner sc1=new Scanner(System.in);
}
class Student3 extends Details
{
	private int mar1;private int mar2;private int mar3;
	
	public Student3(String name, int age, String gender)
	{
		this.name=name;
		this.age=age;
		this.gender=gender;
	}
	public void display()
	{		
		System.out.println("Enter the First Mark");
		 mar1=sc1.nextInt();
		System.out.println("Enter the Second Mark");
		int mar2=sc1.nextInt();
		System.out.println("Enter the Third Mark");
		int mar3=sc1.nextInt();
		
		int total = mar1+mar2+mar3;
		double avg=(float)(total/3);
		
		System.out.println("**************************");
		System.out.println("     Student Details");
		System.out.println("**************************");
		
		System.out.println("The Student Name   :"+name);
		System.out.println("The age of Student :"+age);
		System.out.println("Student Gender     :"+gender);
		System.out.println("Total Mark         :"+total);
		System.out.println("Average of mark    :"+avg);
		
		System.out.println("**************************");
	}
}
class Teacher extends Details
{
	private String sub1;private String sub2;private String sub3;
	public Teacher(String name, int age, String gender)
	{
		this.name=name;
		this.age=age;
		this.gender=gender;
	}
	public void display()
	{
		System.out.println("Enter the First Subject");
		 sub1=sc1.next();
		System.out.println("Enter the Second Subject");
		 sub2=sc1.next();
		System.out.println("Enter the Third Subject");
		 sub3=sc1.next();
		System.out.println("Enter the Salary");
		int salary=sc1.nextInt();
		
		double Ta=(salary*10)/100;
		double Hra=(salary*17)/100;
		
		double gross=Ta+Hra+salary;
		
		double Pf=(salary*10)/100;
		double Pt=(salary*7)/100;
		double It=(salary*9.5f)/100;
		
		float cal=(float)(Pf+Pt+It);
		
		float result=(float)(gross-cal);
		
		System.out.println("******************************");
		System.out.println("       Teacher Details");
		System.out.println("******************************");
		
		System.out.println("The Teacher Name is 	 :"+name);
		System.out.println("Teacher age         	 :"+age);
		System.out.println("Teacher gender      	 :"+gender);
		System.out.print("Taching Subject          :"+sub1);
		System.out.print(", "+sub2);
		System.out.println(", "+sub3);
		System.out.println("gross Salary is		 :"+gross);
		System.out.println("Net Salary is		 :"+result);
		System.out.println("******************************");
	}	
}
class Doctor extends Details
{
	private String specialision;private int experience;private long salary;
	public Doctor(String name, int age, String gender)
	{
		this.name=name;
		this.age=age;
		this.gender=gender;
	}
	public void display()
	{
		System.out.println("Enter the Specialision");
		 specialision=sc1.next();
		System.out.println("Enter the Experience");
		 experience=sc1.nextInt();
		System.out.println("Enter the Salary");
		long salary=sc1.nextLong();
		
		double Ta=(salary*10)/100;
		double Hra=(salary*17)/100;
		
		double gross=Ta+Hra+salary;
		
		double Pf=(salary*10)/100;
		double Pt=(salary*7)/100;
		double It=(salary*9.5f)/100;
		
		float cal=(float)(Pf+Pt+It);
		
		float result=(float)(gross-cal);
		
		System.out.println("*************************************");
		System.out.println("            Doctor Details");
		System.out.println("*************************************");
		System.out.println("Doctor name   		 :"+name);
		System.out.println("Doctor age is 		 :"+age);
		System.out.println("Doctor gender 		 :"+gender);
		System.out.println("Doctor specialision      :"+specialision);
		System.out.println("Doctor Experience 	 :"+experience);
		System.out.println("gross Salary is		 :"+gross);
		System.out.println("Net Salary is		 :"+result);
		System.out.println("*************************************");
	}	
}
public class Person 
{
	public static void main(String[] args) 
	{
		char ch='S';
		do
		{
		//Person pa=new Person();
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the Name");
		String name=sc.next();
		System.out.println("Enter the age");
		int age=sc.nextInt();
		System.out.println("Enter the Gender");
		String gender=sc.next();
		System.out.println("Select your options");
		System.out.println("1.Student");
		System.out.println("2.Teacher");
		System.out.println("3.Doctor");
		String option=sc.next();
		
		if(option.equals("Student"))
		{
		Student3 stu=new Student3(name,age,gender);
		stu.display();
		}
		else if(option.equals("Teacher"))
		{
			Teacher tc=new Teacher(name,age,gender);
			tc.display();
		}
		else if(option.equals("Doctor"))
		{
			Doctor dc=new Doctor(name,age,gender);
			dc.display();
		}
		System.out.println("Do you know about another person details click S");
		ch=sc.next().charAt(0);
	}
		while(ch=='S');
		System.out.println("you press invaild character plz enter vaild char");
}
}
