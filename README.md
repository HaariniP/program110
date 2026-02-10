# program110
from functools import reduce
employees = {"Ravi": 45000, "Anita": 72000, "Karthik": 52000, "Priya": 38000, "Suresh": 61000}
print("Original:", employees)
updated_salaries = dict(map(lambda item: (item[0], int(item[1]*1.10)), employees.items()))
print("After 10% hike:", updated_salaries)
eligible = dict(filter(lambda item: item[1] >= 50000, updated_salaries.items()))
print("Eligible >=50000:", eligible)
total_salary = reduce(lambda x, y: x+y, updated_salaries.values())
print("Total Salary:", total_salary)
