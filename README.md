# MVCProject
public class EmployeeModel
{

    public int EmployeeId;

    public int getEmployeeId() {
        return EmployeeId;
    }

    public void setEmployeeId(int newEmployeeId) {
        this.EmployeeId = newEmployeeId;
    }
        

    public String Name;

    public String getName() {
        return Name;
    }

    public void setName(String newName) {
        this.Name = newName;
    }
        

    public String Address;

    public String getAddress() {
        return Address;
    }

    public void setAddress(String newAddress) {
        this.Address = newAddress;
    }
        

    public String Designation;

    public String getDesignation() {
        return Designation;
    }

    public void setDesignation(String newDesignation) {
        this.Designation = newDesignation;
    }


    public double Salary;

    public double getSalary() {
        return Salary;
    }

    public void setSalary(double newSalary) {
        this.Salary = newSalary;
    }

public class EmployeeController {



    public String AddEmployee()

    {

        EmployeeView employee = new EmployeeView();

        dbContext.Employee.Add(employee);

    }



    public String EditEmployees(int id)

    {

        EmployeeView employee = new EmployeeView();

        dbContext.Entry(employee).State = System.Data.EntityState.Modified;





    }



    public String Delete(int id)

    {

        EmployeeView employee = new EmployeeView();

        dbContext.Employee.Remove(employee);



    }


public class EmployeeView

{

    public Employee Employee;



    public Employee getEmployee() {

        return Employee;

    }



    public void setEmployee(Employee newEmployee) {

        this.Employee = newEmployee;

    }

}

