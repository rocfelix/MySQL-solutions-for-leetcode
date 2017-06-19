# Big Countries

select name, population, area
from World
where population > 25000000
or area > 3000000

# Duplicate Emails

select distinct p1.Email from Person p1
inner join Person p2
on p1.Email=p2.Email 
where p1.Id <> p2.Id

# Combine Two Tables

Select Person.FirstName, Person.LastName, Address.City, Address.State
from Person 
left join Address on Person.PersonId=Address.PersonId


# Employees Earning More Than Their Managers

select E1.Name as Employee
from Employee as E1, Employee as E2 
where E1.ManagerId = E2.Id and E1.Salary > E2.Salary

#Customers Who Never Order

select c.Name Customers
from Customers c
where c.Id not in (select customerId from Orders)

