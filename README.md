# Campus Course & Records Manager (CCRM)

CCRM is a Java SE console-based application designed to manage university academic records through an interactive Command Line Interface (CLI).

The project demonstrates a wide range of Java concepts including OOP, Collections, Streams API, NIO.2, exception handling, recursion, file handling, and software design patterns. Data is stored in CSV format for easy readability, backup, and migration.

##  Features

*  **Student Management** → Add, list, update, and deactivate students.
*  **Course Management** → Add, list, update, deactivate, search, and filter courses.
*  **Enrollment & Grading** → Enroll students, enforce credit limits, record marks, and calculate GPA.
*  **Transcripts** → Generate student transcripts with letter grades.
*  **File Operations** → Import/export CSV datasets and create system backups using recursion.
*  **Reports** → GPA distribution, top students, and course enrollment reports.

##  Project Structure

```text
edu.ccrm
├── cli/        → Menu-driven CLI
├── domain/     → Student, Instructor, Course, Enrollment, Enums
├── service/    → Business logic and services
├── io/         → CSV/file import and export
├── util/       → Validators, Comparators, recursive utilities
└── config/     → Singleton AppConfig and builders

datasets/
├── students.csv
├── instructors.csv
├── courses.csv
└── enrollments.csv
```

##  Technical Demonstrations

### Core Java

* Primitive data types and operators
* if, if-else, nested if, and switch
* for, while, do-while, and enhanced for loops
* break, continue, and labeled statements
* Arrays and Arrays utility methods
* String operations such as substring, split, join, equals, and compareTo

###  Object-Oriented Programming

* Encapsulation
* Inheritance
* Abstraction
* Polymorphism
* Constructors and super calls
* Method overloading and overriding
* Access modifiers
* Upcasting and downcasting
* instanceof
* Immutable classes
* Nested and inner classes
* Interfaces and default methods

###  Lambdas & Functional Programming

* Lambda expressions
* Functional interfaces
* Comparator
* Predicate
* Java Streams

###  Design Patterns

* **Singleton** → AppConfig
* **Builder** → Course.Builder
* **Builder** → Transcript.Builder

###  Exception Handling

* Checked and unchecked exceptions
* Custom exceptions
* try/catch/finally
* Multi-catch
* throw and throws
* Assertions

###  Java APIs

* **NIO.2** → Path, Files, copy, move, delete
* **Streams API** → Filtering, mapping, GPA aggregation
* **Date/Time API** → Enrollment dates and backup timestamps
* **Recursion** → Computing backup directory size

##  Datasets

Sample datasets are available in the `datasets/` directory:

* `students.csv`
* `instructors.csv`
* `courses.csv`
* `enrollments.csv`

### Example students.csv

```csv
id,regNo,fullName,email,status,enrollmentDate
1,REG1001,John Doe,john@example.com,ACTIVE,2023-09-01
2,REG1002,Jane Smith,jane@example.com,ACTIVE,2023-09-02
```

##  Running the Project

### Prerequisites

* Java JDK 17 or later
* VS Code or any Java-compatible IDE

### Compile

#### Linux / macOS

```bash
javac -d bin src/edu/ccrm/**/*.java
```

#### Windows PowerShell

```powershell
dir -Recurse -Filter *.java | ForEach-Object { $_.FullName } > sources.txt
javac -d bin @sources.txt
```

### Run

```bash
java -cp bin edu.ccrm.cli.MainCLI
```

### Run with Assertions

```bash
java -ea -cp bin edu.ccrm.cli.MainCLI
```

##  CLI Demo Flow

```text
1. Manage Students
2. Manage Courses
3. Enrollment & Grading
4. Reports
5. Import/Export Data
6. Backup & Utilities
0. Exit
```

Typical workflow:

1. Import datasets from the `datasets/` folder.
2. Manage students and courses.
3. Enroll students in courses.
4. Record marks and calculate GPA.
5. Generate student transcripts.
6. Export updated datasets.
7. Create system backups.
8. Generate academic reports.

##  Java Platform Notes

### Evolution of Java

| Year | Version  | Major Features            |
| ---- | -------- | ------------------------- |
| 1995 | Java 1.0 | Initial Java release      |
| 2004 | Java 5   | Generics, Annotations     |
| 2011 | Java 7   | Try-with-resources, NIO.2 |
| 2014 | Java 8   | Lambdas, Streams          |
| 2017 | Java 9   | Java Modules              |
| 2021 | Java 17  | LTS release               |
| 2023 | Java 21  | LTS release               |

### Java Editions

| Edition        | Scope                     | Use Cases                    |
| -------------- | ------------------------- | ---------------------------- |
| **Java SE**    | Core libraries, JVM, APIs | Desktop and CLI applications |
| **Jakarta EE** | Enterprise and web APIs   | Web applications and servers |
| **Java ME**    | Lightweight Java platform | Embedded/mobile applications |

### Java Architecture

```text
JDK
├── Development Tools
├── Compiler (javac)
└── JRE
    ├── Java Libraries
    └── JVM
        └── Executes Java Bytecode
```

* **JDK** → Used to develop and compile Java applications.
* **JRE** → Provides the runtime environment and libraries.
* **JVM** → Executes Java bytecode and provides platform independence.

##  Setup

### Install Java on Windows

1. Install a Java JDK.
2. Configure `JAVA_HOME`.
3. Add Java to the system `PATH`.
4. Verify the installation:

```bash
java -version
javac -version
```

### VS Code

Install the **Extension Pack for Java** and open the project folder.

You can compile using `Ctrl + Shift + B` or run `MainCLI.java` using the Run button.

##  Syllabus → Code Mapping

| Concept           | Implementation                                                          |
| ----------------- | ----------------------------------------------------------------------- |
| Encapsulation     | Student.java – private fields, getters/setters                          |
| Inheritance       | Person.java → Student.java, Instructor.java                             |
| Abstraction       | Person.java – abstract class                                            |
| Polymorphism      | TranscriptService and toString() overrides                              |
| Singleton         | AppConfig.java                                                          |
| Builder           | Course.Builder, Transcript.Builder                                      |
| Enums             | Semester.java, Grade.java                                               |
| Custom Exceptions | DuplicateEnrollmentException.java, MaxCreditLimitExceededException.java |
| Streams           | CourseService.filterByDepartment()                                      |
| Recursion         | BackupService.computeDirectorySize()                                    |
| Assertions        | Enrollment.java                                                         |

##  Technologies Used

**Java SE • OOP • Collections • Streams API • NIO.2 • CSV • Exception Handling • Recursion • Design Patterns • Date/Time API**

##  Objective

CCRM combines a practical academic record management system with a comprehensive demonstration of Java programming concepts, from fundamental language features to advanced APIs and design patterns.

##  Future Enhancements

* Database integration
* GUI/Web interface
* User authentication
* Role-based access control
* REST API integration
* Automated testing
* PDF transcript generation

##  License

This project is created for educational and academic purposes.
