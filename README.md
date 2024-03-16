<h1 align="center">

<br>

<p align="center">


</p>

<br>

<br>

</h1>

<h2 align="center">Eclinic</h2>


## Project Overview 🎊
<h6> Eclinic- Project in Java, Spring Boot, Angular, H2, Docker creating a database to assist patients in managing their appointments at an eClinic. The system helps in the functioning of the web application related to online appointment scheduling, accessible via a web browser. The primary function of the system is to enable patients to create their own accounts and access them remotely. Patients can use their accounts to schedule appointments, view available time slots, confirm appointments, receive reminders of their upcoming visits, and verify their attendance.Additionally, the system allows doctors to manage their schedules by viewing the number of patients they have each day and accessing their appointment calendars. </h6>

## Tech/framework used 🔧

| Tech                                                    | Description                              |
| ------------------------------------------------------- | ---------------------------------------- |
| Java                                                 | an object-oriented programming language used to build primary structure of the help chef app    |
| Spring Boot                                          | a java-based framework used for creating spring-based applications in Java in short time bereft of being tied to a specific platform, which enables chef help to run locally on any devices even without an internet access.   |
| Angular                                              | an open- source front-end JavaScript framework for developing web applications using HTML, CSS and TypeScript  |
| H2                                                   | a lightweight Java SQL database, which can run entirely in-memory or with disk-storage |
| Docker                                               | an open source platform for quickly creating, deploying, managing and testing Help Chef on any platform   |
| Java Script                                          | a scripting language used to create dynamic web pages for help chef application  |


## Screenshots 📺

<p align="center">
<h2>
  Not available at the moment, still in construction. 
</h2>
  
</p>


## Code Example/Issues 🔍


## Installation 💾

## UML Diagrams 📈
<h4> Use case diagram </h4>
<h5> A use case diagram is a UML diagram that shows us in the form of scenarios how a system or software interacts with individuals, organizations, or external systems carried for the purposes of this diagram the name of actors. It transmits how the actor uses the system to achieve a specific goal. It doesn't implement details, attributes, and user values. Without an actor, creating a use case diagram would be impossible as the main goal is to show how to use the system. Thus, it allows you to designate programmer, the goals that a given software user will want to achieve. These diagrams are used to supplement more detailed documentation. For an eClinic system, the use case diagram would showcase how various actors, such as patients, doctors, and administrators, interact with the system to achieve their objectives. Examples of use cases might include scheduling appointments, managing patient records, viewing available time slots, and sending appointment reminders. Here's a brief overview of potential use cases for an eClinic system:
</h5>
<h6>
  Patient:

Schedule appointment
View appointment history
Cancel appointment
Receive appointment reminders
Doctor:

View daily schedule
Update availability
Access patient records
Mark appointments as attended
Administrator:

Manage user accounts
Generate reports
Configure system settings
</h6>


<h4> Class diagram </c4>
<h5> A class diagram is a UML diagram that is considered by many to be one of the most useful diagrams because they allow us to reproduce the structure very precisely specific system. A class diagram uses information about its class for this purpose,
attribute, operation, and relations between them, e.g. class: human, attribute: eye color, height or weight, and the operation will be some activity, e.g. driving a car. The shape construction of this diagram is divided into three rows and is in the form of a rectangle. The top row contains information about the class name, the middle one tells us about the class's attributes and the bottom row has pieces of information about the methods or operations that the class can perform. We must also remember that classes also have access modifiers, they are visible only to e.g. network administrator or for all users, depending on which symbol we choose ( Public (+) or Private (-)). In our project, we have e.g. class name as the user, attributes are id, name, surname, e-mail, nick, and the operations are login and sign. For an eClinic system, the class diagram would illustrate the various classes, their attributes, and operations involved in managing the system. Here's a revised example: </h5>
<h6>
  
A class diagram is a UML diagram that precisely represents the structure of a specific system. It utilizes classes, attributes, operations, and relationships to depict the system's architecture. Each class in the diagram is represented by a rectangle divided into three rows.

For an eClinic system, the class diagram would illustrate the various classes, their attributes, and operations involved in managing the system. Here's a revised example:

Class: Patient

Attributes:
id: int
name: String
surname: String
email: String
phone: String
Operations:
scheduleAppointment()
cancelAppointment()
getAppointmentHistory()
Class: Doctor

Attributes:
id: int
name: String
specialization: String
Operations:
viewDailySchedule()
updateAvailability()
accessPatientRecords()
Class: Appointment

Attributes:
id: int
date: Date
time: Time
patient: Patient
doctor: Doctor
Operations:
confirmAppointment()
cancelAppointment()
Class: Administrator

Attributes:
id: int
username: String
password: String
Operations:
manageUserAccounts()
generateReports()
configureSystemSettings()
</h6>


<h4> Activity diagram </c4>
<h5> An activity diagram is a UML diagram that is used to model activities and scope responsibility of system components or users. It is otherwise known as an interaction diagram. Its primary function is to show the sequence of steps. These steps are performed by the modeled part of the system. It shows in the form of elements the behavior of the system, but where, the most important element is the activity. In this way, it shows the behavioral aspects of our system by using activities that the user, administrator, or server performs. The activity diagram was created by using: https://www.visual-paradigm.com. </h5>
<h6>
  An activity diagram for an eClinic system depicts the sequence of steps performed by various users, administrators, and the server to model activities and responsibilities within the system. Here's an outline of how such a diagram might be structured:

Patient Booking Appointment:

Start
Enter credentials
View available appointments
Select desired appointment
Confirm appointment booking
End
Doctor Managing Schedule:

Start
Login
View daily schedule
Update availability
End
Administrator Managing System:

Start
Login
Manage user accounts
Generate reports
Configure system settings
End
System Processing Appointment:

Start
Receive appointment request
Check availability
Confirm appointment
Send confirmation to patient
End
</h6>


## System architecture 🗼
<h4> C4 diagram </h4>
<h5> C4 level model diagram stands for context, containers, components, and code. It is a diagram that shows a hierarchical set of software architecture and is a great tool to communicate the planning process of a software system. Help-chef project is beeing created using many programming languages and technologies. Backend of the application is beeing implemented in Java. Spring Framework is responsible for business side of the system and enables double sided communication with H2 database.
Connection with server follows with REST API architecture style. Web application is beeing created using JavaScript Framework - Angular. </h5>
<h6>
  For the eClinic project, the C4 model diagram can be used to represent the hierarchical set of software architecture components. Here's how it might look:

1. Context Diagram:
eClinic System
Represents the entire system as a single box.
External actors or systems interact with the eClinic system.
Shows the boundaries and external dependencies of the system.
Communication with external systems follows REST API architecture style.
2. Container Diagram:
Backend Container (Java with Spring Framework)

Contains:
Java
Spring Framework
Business logic
H2 Database (for development)
Responsible for handling business logic and data processing.
Communicates with the database using Spring Data.
Database Container (H2 Database)

Contains:
H2 Database
Stores and manages application data.
Accessed by the backend container via JDBC or Spring Data JPA.
Frontend Container (JavaScript Framework - Angular)

Contains:
Angular framework
HTML/CSS/JavaScript
Responsible for the presentation layer and user interaction.
Communicates with the backend via RESTful APIs.
3. Component Diagram:
Backend Components

Controllers: Handle incoming HTTP requests and delegate to services.
Services: Implement business logic and interact with repositories.
Repositories: Interface with the database to perform CRUD operations.
Security: Components responsible for authentication and authorization.
Frontend Components

Components: Angular components for different views and UI elements.
Services: Angular services to handle data retrieval and manipulation.
HTTP Client: Interacts with the backend REST API to fetch and send data.
Routing: Manages navigation between different views.
4. Code Diagram:
Java Codebase
Contains Java classes for controllers, services, repositories, and security configurations.
Follows Spring Framework conventions and patterns.
JavaScript Codebase (Angular)
Contains TypeScript classes for components, services, and routing modules.
Follows Angular framework conventions and patterns.
This C4 model diagram provides a high-level overview of the eClinic system's architecture, from its context to its implementation details, facilitating communication and understanding among stakeholders and development teams.
</h6>


## Available scripts 💡

| Command                   | Description                   |     |
| ------------------------- | ----------------------------- | --- |
| `npm run start`           | Open local server             |     |
| `npm run build`           | Create optimized build        |     |
| `npm run test`            | Run tests                     |     |
