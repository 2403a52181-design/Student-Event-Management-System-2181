students = \[]



def add\_student():

&#x20;   student\_id = input("Enter Student ID: ")

&#x20;   name = input("Enter Student Name: ")

&#x20;   age = int(input("Enter Age: "))

&#x20;   course = input("Enter Course: ")

&#x20;   marks = float(input("Enter Marks: "))



&#x20;   student = {

&#x20;       "id": student\_id,

&#x20;       "name": name,

&#x20;       "age": age,

&#x20;       "course": course,

&#x20;       "marks": marks

&#x20;   }



&#x20;   students.append(student)

&#x20;   print("\\nStudent added successfully!")





def view\_students():

&#x20;   if len(students) == 0:

&#x20;       print("\\nNo students available.")

&#x20;       return



&#x20;   print("\\n========== STUDENT DETAILS ==========")



&#x20;   for student in students:

&#x20;       print("------------------------------")

&#x20;       print("ID     :", student\["id"])

&#x20;       print("Name   :", student\["name"])

&#x20;       print("Age    :", student\["age"])

&#x20;       print("Course :", student\["course"])

&#x20;       print("Marks  :", student\["marks"])





def search\_student():

&#x20;   student\_id = input("Enter Student ID to search: ")



&#x20;   for student in students:

&#x20;       if student\["id"] == student\_id:

&#x20;           print("\\nStudent Found!")

&#x20;           print("ID     :", student\["id"])

&#x20;           print("Name   :", student\["name"])

&#x20;           print("Age    :", student\["age"])

&#x20;           print("Course :", student\["course"])

&#x20;           print("Marks  :", student\["marks"])

&#x20;           return



&#x20;   print("\\nStudent not found.")





def delete\_student():

&#x20;   student\_id = input("Enter Student ID to delete: ")



&#x20;   for student in students:

&#x20;       if student\["id"] == student\_id:

&#x20;           students.remove(student)

&#x20;           print("\\nStudent deleted successfully!")

&#x20;           return



&#x20;   print("\\nStudent not found.")





while True:



&#x20;   print("\\n===================================")

&#x20;   print("     STUDENT MANAGEMENT SYSTEM")

&#x20;   print("===================================")

&#x20;   print("1. Add Student")

&#x20;   print("2. View Students")

&#x20;   print("3. Search Student")

&#x20;   print("4. Delete Student")

&#x20;   print("5. Exit")

&#x20;   print("===================================")



&#x20;   choice = input("Enter your choice: ")



&#x20;   if choice == "1":

&#x20;       add\_student()



&#x20;   elif choice == "2":

&#x20;       view\_students()



&#x20;   elif choice == "3":

&#x20;       search\_student()



&#x20;   elif choice == "4":

&#x20;       delete\_student()



&#x20;   elif choice == "5":

&#x20;       print("Thank you!")

&#x20;       break



&#x20;   else:

&#x20;       print("Invalid choice!")

