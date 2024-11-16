# PYTHON_OOPS_AND_MODULE
Python solutions demonstrating object-oriented programming with hierarchical inheritance and module-based class design.

# Build a program to manage a university's course catalog. You want to define a base class Course that has the following properties: course_code: a string representing the course code (e.g., "CS101") course_name: a string representing the course name (e.g., "Introduction to Computer Science") credit_hours: an integer representing the credit hours for the course (e.g., 3) You also want to define two subclasses CoreCourse and ElectiveCourse, which inherit from the Course class. CoreCourse should have an additional property required_for_major which is a boolean representing whether the course is required for a particular major. ElectiveCourse should have an additional property elective_type which is a string representing the type of elective (e.g., "general", "technical", "liberal arts"). 

class Course:

    def __init__(self, course_code, course_name, credit_hours):
        self.course_code = course_code
        self.course_name = course_name
        self.credit_hours = credit_hours

class CoreCourse(Course):

    def __init__(self, course_code, course_name, credit_hours, required_for_major):
        Course.__init__(self, course_code, course_name, credit_hours)
        self.required_for_major = required_for_major

class ElectiveCourse(Course):

    def __init__(self, course_code, course_name, credit_hours, elective_type):
        Course.__init__(self, course_code, course_name, credit_hours)
        self.elective_type = elective_type

core_course1 = CoreCourse("CS101", "Introduction to Computer Science", 3, True)

print(f"\nCore Course: {core_course1.course_code} - {core_course1.course_name}")

print(f"Credit Hours: {core_course1.credit_hours}")

print(f"Required for Major: {'Yes' if core_course1.required_for_major else 'No'}")

elective_course1 = ElectiveCourse("MATH201", "Calculus", 4, "technical")

print(f"\nElective Course: {elective_course1.course_code} - {elective_course1.course_name}")

print(f"Credit Hours: {elective_course1.credit_hours}")

print(f"Elective Type: {elective_course1.elective_type}")

![q1](https://github.com/user-attachments/assets/593dc8d9-9f43-4df4-ac86-cb4a8a47323e)

