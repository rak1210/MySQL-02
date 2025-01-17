1. User:

UserID (Primary Key)
FirstName
LastName
Email (Unique)
PasswordHash
Role (e.g., Student, Instructor, Admin)
DateOfBirth
RegistrationDate


2. Class:

ClassID (Primary Key)
ClassName
Description
InstructorID (Foreign Key referencing UserID)
StartDate
EndDate
Duration (in hours)
Price


3. Enrollment:

EnrollmentID (Primary Key)
UserID (Foreign Key referencing UserID)
ClassID (Foreign Key referencing ClassID)
EnrollmentDate
Status (e.g., Enrolled, Completed, Dropped)


4. Lesson:

LessonID (Primary Key)
ClassID (Foreign Key referencing ClassID)
LessonTitle
LessonDescription
LessonDate
Duration (in minutes)


5. Assignment:

AssignmentID (Primary Key)
ClassID (Foreign Key referencing ClassID)
AssignmentTitle
AssignmentDescription
DueDate


6. Submission:

SubmissionID (Primary Key)
AssignmentID (Foreign Key referencing AssignmentID)
UserID (Foreign Key referencing UserID)
SubmissionDate
Grade


Relationships: 

User to Enrollment: One-to-Many (One user can enroll in multiple classes)
Class to Enrollment: One-to-Many (One class can have multiple enrollments)
User to Class: Many-to-Many (Users can be enrolled in multiple classes and classes can have multiple users)
Class to Lesson: One-to-Many (One class can have multiple lessons)
Class to Assignment: One-to-Many (One class can have multiple assignments)
Assignment to Submission: One-to-Many (One assignment can have multiple submissions)
