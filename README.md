# printing-employee-details
def get_employee_details():
    name = input("enter employee name: ")
    emp_id = input("enter employee ID: ")
    department = input("enter department: ")
    basic_salary = float(input("enter basic salary: "))
    return name , emp_id, department, basic_salary

def calculate_salary(basic_salary):
    hra = basic_salary * 0.20
    da = basic_salary * 0.10
    pf= basic_salary * 0.12
    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf
    return hra, da, pf, gross_salary, net_salary

def print_salary_slip(name, emp_id, department, basic, hra,da, pf, gross, net):
    print("n=================== EMPLOYEE SALARY SLIP ========================")
    print("employee name :", name)
    print("employee ID   ;", emp_id)
    print("department    :", department)
    print("=================================================================")
    print("Basic Salary : rs.", basic)
    print("HRA(20%)     : rs.", hra)
    print("DA(10%)      : rs.", da)
    print("PF deduction : rs.", pf)
    print("------------------------------------------------------------------")
    print("Gross Salary : rs.", gross)
    print("net salary:rs: rs.", net)
    print("=================================================================")
    
    name, emp_id, department, basic = get_employee_details()
    hra, da, pf, gross, net = calculate_salary(basic)
    print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)
    OUTPUT:
     ==============
Enter employee name: cathrine
Enter employee ID: 39
Enter department: computer science
Enter basic salary: 50000

=================== EMPLOYEE SALARY SLIP ========================
Employee Name : cathrine
Employee ID   : 39
Department    : computer science
===============================================================
Basic Salary : Rs. 50000.0
HRA (20%)    : Rs. 10000.0
DA (10%)     : Rs. 5000.0
PF Deduction : Rs. 6000.0
---------------------------------------------------------------
Gross Salary : Rs. 65000.0
Net Salary   : Rs. 59000.0
===============================================================



        
