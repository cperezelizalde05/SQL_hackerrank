# Top Earners

We define an employee's total earnings to be their monthly  worked, and the maximum total earnings to be the maximum total earnings for any employee in the Employee table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as  space-separated integers.

INPUT FORMAT

The Employee table containing employee data for a company is described as follows:

[![Problem](https://s3.amazonaws.com/hr-challenge-images/19629/1458557872-4396838885-ScreenShot2016-03-21at4.27.13PM.png "Problem")](https://www.hackerrank.com/challenges/earnings-of-employees/problem "Problem")

where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is the their monthly salary.

SAMPLE INPUT

[![Sample](https://s3.amazonaws.com/hr-challenge-images/19631/1458559098-23bf583125-ScreenShot2016-03-21at4.32.59PM.png "Sample")](https://www.hackerrank.com/challenges/earnings-of-employees/problem "Sample")


SAMPLE OUTPUT

[![Sample Output](https://s3.amazonaws.com/hr-challenge-images/19631/1458559218-9f37585c7a-ScreenShot2016-03-21at4.49.23PM.png "Sample Output")](https://www.hackerrank.com/challenges/earnings-of-employees/problem "Sample Output")

69952 1
**EXPLANATION**

The table and earnings data is depicted in the following diagram: 

The maximum earnings value is 69952 . The only employee with earnings  is = 69952 Kimberly, so we print the maximum earnings value (69952) and a count of the number of employees who have earned $69952 (which is ) as two space-separated values.

**Solución**
SELECT MAX(salary*months) as max_salary, COUNT(*) FROM employee WHERE salary*months = (SELECT MAX(salary*months) FROM employee);
