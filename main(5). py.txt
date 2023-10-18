class student:
  
 def __init__(self,name,roll_number, cgpa):
   self.name = name 
   self.roll_number = roll_number 
   self.cgpa = cgpa


def sort_students(student_list):
  
  sorted_students = sorted(student_list,
    key=lambda student:student.cgpa,
                       reverse=True)
  return sorted_students



students = [
  student("mari","A145",7.8),
  student("arun","A167",8.9),
  student("ajay","A178", 9.1),
  student("Raja","A134",9.9),
]

sorted_student = sort_students(students)


for student in sorted_student:
  print("Name: {}, Roll number:{}, CGPA: {}".format(student.name,
student.roll_number,
student.cgpa))