# E-Exam System Requirements

## Overview
E-Exam is a System for students to get their exams online. **The Controller** manages the offers for buying spaces on the system (specifies the costs for each offer) for each faculty depends on the number of Students and Professors in the faculty.

**The Dean** for each faculty selects the appropriate system for calculating students’ grades (either **GPA** or **Common evaluation**), buys a space on the system, is responsible for adding, editing subjects and professors and making an approval for the professors.

**Professors** prepare for their subjects’ exams with adding and editing questions and identifying the correct answer and the level of difficulty for each question.

**Students** take the exam with different random questions and the results are stored to be shown for the student and professor.

## Types of Users
1. **Controller:** manages the offers for buying a space on the system
2. **Dean:** is basically a professor with Administrating Authentications.
3. **Professor:** is responsible for The Structure of the Exam and its content.
4. **Student:** takes the Exam and then directly notified with his own result.

## **Controller**
1. Manages the offers that the system provides for buying spaces on it (specifies costs for each offer).  
2. Views The List of the Deans and Faculties, and Approves the Sign up Requests.

## **Dean**
1. Buys a space on the system (its cost depends on the number of the Students and Professors) and pays for it.
2. Selects the appropriate system for calculating students’ grades.
3. Specifies how the GPA will be calculated for the students’ final grades (either A=3.7 or A=3.6 and so on).
4. Specifies how many exams will be held during each semester
5. Responsible for adding, editing subjects and professors and making an approval for the professors.
6. Adding, Editing the Levels and Departments of the Faculty.
7. Adding, Editing the Subjects of each level and department.
8. Specifies the subjects for each professor.
9. Views The List of the Professors, and Approves the Sign up Requests.
10. All Privileges of the Professor.

## **Professor**
1. Adding and editing chapters for each subject that he teaches and detects the number of questions of each chapter.
2. Specifies the Category of each question, which describe the difficulty of the Questions.
3. Organizing the structure of the exam.
4. Adding, Editing Questions and Identify the Correct Answer, and those Questions should be published for the students as Questions Bank.
5. Determines the allowed time for finishing the exam.
6. Determines the Exam start time and end time, so that the student cannot access the Exam before or after its time.
7. Shows The Results of the Students for his Subjects.
8. Can know how many times each Question is answered correctly and how many wrongly.
9. Can know how many times each answer is selected for each question.
10. Can add Open Ended Questions, which the student answers by writing the answer, and Evaluates the answer manually.
11. Has a page for managing students including some data.  
**Example:**  

| Student ID | Student Name     | Subject Name | Date & Time | Number of Questions | Right Answers | Wrong Answers |
| :---: | :---: | :---: | :---: | :--: | :--: | :--: |
| **1234** | Toka Muhammed | Mathematics | 02/10/2020 05:50 a.m. | 60 | 58 | 2 |

12. Adds the required degrees as yearly performance scores to the student’s final results. 

## Student
1. Signs Up and Selects his Level and Department.
2. Signs In and Selects the Subject to start his Exam
3. Finish The Exam, Submit it and show the Result and his Previous Exams’ Results.
4. Is notified of his Rank among his Level.
5. Is notified when the Exams Final results appear (for the exams that include open Ended Questions).
6. Can enter the exam again with their submitted answers and view the correct answers for their wrong questions (view correct choices).  
**Example:**  
> Q1) We can create a clone of singleton object.  
> a) True  
> b) False  
> **Right Answer: A.**

9. Receives a report of his own, including his grades in each subject.

## The Structure of the Exam 

1. The types of Question are MCQ, True & False and Open-Ended Questions.
2. The Professor specifies how many questions that the Exam must have.
3. The Professor specifies how many questions included from each chapter that the Exam must have.
4. The Questions are partitioned into Three Categories, A, B & C depending on the Difficulty Level.
5. The Professor Specifies number of Questions of each Category from each Chapter of each type.  
**Ex:**
    * 3 Questions MCQ of Category A from Chapter 1, 
    * 4 Questions MCQ of Category B from Chapter 1,
    * 4 Questions MCQ of Category C from Chapter 1,
    * 4 Questions T&F of Category A from Chapter 1,
    * 3 Questions T&F of Category B from Chapter 1,
    * 2 Questions T&F of Category C from Chapter 1,
    And so on for each Chapter.
6. Each student gets random Questions According to the previous constraints that Professor set.
7. The MCQ Choices should be arranged randomly, so that, the order of answer will differ from student to another.  
**Ex:**
Consider a Question with choices (20, 30, 40 and 50). The Choices should appear for the different students like this:
    * Student 1: &nbsp; &nbsp; &nbsp; A) 20 &nbsp; &nbsp; B) 30 &nbsp; &nbsp; C) 40 &nbsp; &nbsp; D) 50
    * Student 2: &nbsp; &nbsp; &nbsp; A) 50 &nbsp; &nbsp; B) 40 &nbsp; &nbsp; C) 30 &nbsp; &nbsp; D) 20
    * Student 3: &nbsp; &nbsp; &nbsp; A) 30 &nbsp; &nbsp; B) 20 &nbsp; &nbsp; C) 50 &nbsp; &nbsp; D) 40
    * Student 4: &nbsp; &nbsp; &nbsp; A) 50 &nbsp; &nbsp; B) 20 &nbsp; &nbsp; C) 40 &nbsp; &nbsp; D) 30

## Considerations
Consider these points while developing the System  
1. Sign Up and Sign in Pages. Sign up for Professors, who need Approval from The Admin, and for Students.
2. The Authentication of each page, ex… student cannot add Questions, users cannot get into Log in or Sign up pages.
3. Data Validation for every input in the System, prevent SQL Injection and Consider Basic Security Concepts.
4. If allowed Time of the Exam is finished, then the Exam is automatically submitted.
5. The Professor can add multiple Questions in one Request.
6. The Professor can add or edit questions for only his Subjects.
7. The Professor can see The Results of the Students for only his Subjects
8. The Student can see only his Result.
9. The Student cannot submit the Exam more than one Time.
10. Develop the system Multilingual (English and Arabic).
11. Question can be text, image, audio, video or compilation of them.
12. MCQ Questions can have more than one correct answer and the student must select all the correct choices.
13. Calculating GPA grades varies depending on the faculty system.
14. Students who did not register the subjects are prevented from taking the exam.

## System Features
1. The system stores the Attendance and the Absence of the students who do/do not take the Exam.
2. The system notifies the students about the Subject’s Exam time.
3. The system provides two methods for calculating final grades either through: common evaluation (Excellent, very good, and so on) or GPA
4. The system provides a rank arranged by students’ degree in each subject within each level.
