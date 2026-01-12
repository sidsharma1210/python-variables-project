# python-variables-project
Basic Python variables examples
Task: Write a Python program that reads three positive integers representing the lengths of the sides of a triangle.
Your program should:
Check whether the given sides form a valid triangle.
A triangle is valid if the sum of any two sides is greater than the third side.
If the sides do not form a valid triangle, print:
Invalid triangle
If the triangle is valid, classify it based on sides:
Equilateral → all three sides are equal
Isosceles → exactly two sides are equal
Scalene → all sides are different
Then classify the triangle based on angles:
Right-angled → square of the longest side equals the sum of squares of the other two sides
Acute → square of the longest side is less than the sum of squares of the other two sides
Obtuse → square of the longest side is greater than the sum of squares of the other two sides
Print the result in the following format:

a,b,c = map(int,input().split())
if a+b <= c or b +c<= a or c+a <= b:
  print("Not valid Triangle")
else:
  if a == b == c:
    side_type = ("Equilateral")
  elif a == b or b == c or c == a:
    side_type = ("Isosceles")
  else:
    side_type = ("scalene")
  x,y,z = sorted([a,b,c])
  if z*z == x*x +y*y:
    angle = ("Right-angled triangle")
  elif z*z < x*x +y*y:
    angle = ("Acute-angled triangle")
  else:
    angle = ("obtuse- Angled triangle")
  print(f"{side_type},{angle}")
