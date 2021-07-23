
public class Company {

	private String Name;

	private String Employees;

	private String Teamlead;

	public String getName() {
		return Name;
	}

	public void setName(String name) {
		Name = name;
	}

	public String getEmployees() {
		return Employees;
	}

	public void setEmployees(String employees) {
		Employees = employees;
	}

	public String getTeamlead() {
		return Teamlead;
	}

	public void setTeamlead(String teamlead) {
		Teamlead = teamlead;
	}

}


import java.util.Scanner;

public class CompanyMain {

	public static void main(String[] args) {
		Company com = new Company();
		Scanner scan = new Scanner(System.in);
		System.out.println("Enter the Company name: ");
		com.setName(scan.nextLine());

		System.out.println("Enter the Employees: ");
		com.setEmployees(scan.nextLine());

		System.out.println("Enter TeamLead: ");
		com.setTeamlead(scan.nextLine());
		boolean isTrue = false;
		String[] ename = com.getEmployees().split(",");
		for (String emp : ename) {
			if (emp.equals(com.getTeamlead())) {
				String teamLead = emp;
				isTrue = true;
			}
		}
		if (!isTrue) {
			System.out.println("Invalid Input");
		} else {
			System.out.println("Name: " + com.getName());
			System.out.println("Employees: " + com.getEmployees());
			System.out.println("Lead: " + com.getTeamlead());
		}
	}

}
