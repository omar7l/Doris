# Lecture Note Sharing Hub Project

The Lecture Note Sharing Hub is a web application designed for the FHNW students to conveniently find and share lecture notes.  
 
It features a comprehensive filtering system that allows students to sort notes by various criteria including module, location, and lecturer.  
 
Users can upload their notes, manage their content, and easily navigate the platform to access the information they need, tailored to their educational requirements. The app supports secure user authentication for students and admins, ensuring a safe exchange of information.

[![License](https://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

> 🚧: **This is a template project**: Make sure you adapt this documentation and the source code in this project according to your needs and use case. Comments are provided with "🚧:". Do not leave these comments in your final submission!

#### Contents:
- [Analysis](#analysis)
  - [Scenario](#scenario)
  - [User Stories](#user-stories)
  - [Use Case](#use-case)
- [Design](#design)
  - [Prototype Design](#prototype-design)
  - [Domain Design](#domain-design)
  - [Business Logic](#business-logic)
- [Implementation](#implementation)
  - [Backend Technology](#backend-technology)
  - [Frontend Technology](#frontend-technology)
- [Project Management](#project-management)
  - [Roles](#roles)
  - [Milestones](#milestones)

### Scenario

The Lecture Note Sharing Hub is a web application designed for the FHNW students to conveniently find and share lecture notes.  

### User Stories
User:
1.	As a User, I want to have a website that is easily accessible.
2.	As a User, I want to have a website that is mobile-friendly.
3.	As a User, I want to create an account.
4.	As a User, I want to delete my user account.
5.	As a User, I want to have the opportunity to change my password or username.
6.	As a User, I want to upload my notes for a specific module.
7.	As a User, I want to edit my notes' title and content.
8.	As a User, I want to delete my notes for a specific module if I don’t want to share them anymore.
9.	As a User, I want to favorite notes so I can see how many favorites they have.
10.	As a User, I want an overview of my favorite notes.
11.	As a User, I want to search for notes by title.
12.	As a User, I want to filter notes by location, degree, and module.
13.	As a User, I want to filter notes by module period and module.
Admin:
14.	As an Admin, I want to delete user accounts.
15.	As an Admin, I want to change usernames for users.
16.	As an Admin, I want to delete notes.
17.	As an Admin, I want to add a module.


### Use Case

![image](https://github.com/omar7l/DorY/assets/115163722/b6e2b86d-aaff-4cda-8261-c6425b862ae7)

User:
[Login] User can log into the web application
[View Own Profile] User can view their own profile.
[Change or Delete Own Username or Password] User can change or delete their username or password.
[Upload Notes] User can upload notes.
[View Notes] User can view notes.
[Search, Filter, and Sort Notes] User can search, filter, and sort notes.
[Delete Notes] User can delete their notes.

Admin:
[Login] Admin can log into the web application.
[View Own Profile] Admin can view their own profile.
[Change or Delete Own Username or Password] Admin can change or delete their username or password.
[View User Profiles] Admin can view user profiles.
[Change Usernames from Users] Admin can change usernames for users.
[Delete User Accounts] Admin can delete user accounts. 
[Delete Notes] Admin can delete uploaded notes.


## Design
The color palette should adhere to the official FHNW colors, ensuring that the application maintains a consistent look and feel with FHNW's websites. Graphics should be a mix of those sourced from FHNW websites and custom-made elements to ensure a cohesive and branded user experience. Typography choices should align with those used by FHNW to maintain consistency across all platforms. The layout should be clean, organized, and easily navigable, mirroring the design principles of FHNW's website. UX design should prioritize ease of use and intuitive navigation, adhering to FHNW's corporate identity guidelines.

### Wireframe

![image](https://github.com/omar7l/DorY/assets/115163722/844c8d66-ad49-480d-98b0-1f412348a469)
![image](https://github.com/omar7l/DorY/assets/115163722/27f8d73e-dae4-4922-b41c-2dea42990526)
![image](https://github.com/omar7l/DorY/assets/115163722/3736cc56-75df-4021-9237-71cba630e614)
![image](https://github.com/omar7l/DorY/assets/115163722/1e0eb2a5-89a5-45f4-982c-45051ea3bbb8)
![image](https://github.com/omar7l/DorY/assets/115163722/33959e46-1031-41de-8f0a-7b110329163b)
![image](https://github.com/omar7l/DorY/assets/115163722/6c079228-c913-492f-b6f1-2869e4c28dea)
![image](https://github.com/omar7l/DorY/assets/115163722/4e1720d5-d054-418f-97d9-3e3097e1dfee)
![image](https://github.com/omar7l/DorY/assets/115163722/9b19a345-b96c-4d3e-b817-4f00df7a88b6)
![image](https://github.com/omar7l/DorY/assets/115163722/e881d32f-411b-4537-8b06-7b334c9025de)
![image](https://github.com/omar7l/DorY/assets/115163722/196670ae-a91c-4c4c-86d7-d16bff4b53db)
![image](https://github.com/omar7l/DorY/assets/115163722/54133036-ce09-4557-b5ce-1715e4b9826b)
![image](https://github.com/omar7l/DorY/assets/115163722/912c12de-f912-46c8-ae9a-76dcb11fef65)




### Domain Design
![image](https://github.com/omar7l/DorY/assets/115163722/eea42af9-28f0-4566-aef7-c142eacc82cd)




### Business Logic 
> 🚧: Describe the business logic for **at least one business service** in detail. If available, show the expected path and HTPP method. The remaining documentation of APIs shall be made available in the swagger endpoint. The default Swagger UI page is available at /swagger-ui.html.

Based on the UC-4, there will be two offers and a standard offer. Given a location, a message is shown accordingly:

- If the location is "Basel", the message is "10% off on all large pizzas!!!"
- If the location is "Brugg", the message is "two for the price of One on all small pizzas!!!"
- Otherwise, the message is "No special offer".

**Path**: [`/api/menu/?location="Basel"`] 

**Param**: `value="location"` Admitted value: "Basel","Brugg".

**Method:** `GET`

## Implementation

We used Spring boot for the backend and budibase to build the frontend. The connections were established using a REST API. 

### Backend Technology

This Web application is relying on [Spring Boot](https://projects.spring.io/spring-boot) and the following dependencies:

- [Spring Boot](https://projects.spring.io/spring-boot)
- [Spring Data](https://projects.spring.io/spring-data)
- [Java Persistence API (JPA)](http://www.oracle.com/technetwork/java/javaee/tech/persistence-jsp-140049.html)
- [H2 Database Engine](https://www.h2database.com)

To bootstrap the application, the [Spring Initializr](https://start.spring.io/) has been used.

Then, the following further dependencies have been added to the project `pom.xml`:

- DB:
```XML
<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
</dependency>
```

- SWAGGER:
```XML
   <dependency>
      <groupId>org.springdoc</groupId>
      <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
      <version>2.3.0</version>
   </dependency>
```

### Frontend Technology

This Web application was developed using Budibase and it is available for preview at

## Execution
> 🚧: Please describe how to execute your app and what configurations must be changed to run it. 

The codespace URL of this Repo is subject to change. Therefore, the Budibase PizzaRP webapp is not going to show any data in the view, when the URL is not updated or the codespace is offline. Follow these steps to start the webservice and reconnect the webapp to the new webservice url. 

> 🚧: This is a shortened description for example purposes. A complete tutorial will be provided in a dedicated lecture.

1. Clone PizzaRP in a new repository.
2. Start your codespace (see video guide at: [link](https://www.youtube.com/watch?v=_W9B7qc9lVc&ab_channel=GitHub))
3. Run the PizzaRP main available at PizzaApplication.java on your own codespace.
4. Set your app with a public port, see the guide at [link](https://docs.github.com/en/codespaces/developing-in-a-codespace/forwarding-ports-in-your-codespace).
5. Create an own Budibase app, you can export/import the existing Pizzeria app. Guide available at [link](https://docs.budibase.com/docs/export-and-import-apps).
6. Update the pizzeria URL in the datasource and publish your app.

## Project Management
For our Lecture Note Sharing Hub project, we used a combination of Scrum and Kanban methodologies to ensure efficient and organised project management. This hybrid approach combined the structure of Scrum with the flexibility of Kanban, allowing us to adapt to changes quickly while remaining focused on deliverables.

We organised our work into three sprints, each meticulously planned and tracked with Jira. During each sprint, we prioritised tasks based on their importance and dependencies to ensure that critical functionalities were developed and tested on time. The sprints facilitated iterative progress by allowing us to incorporate feedback and continuously improve.

Sprint 1 concentrated on foundational elements such as user authentication, basic note management features, and initial database and backend infrastructure configuration.
Sprint 2 focused on improving the user interface, implementing advanced search and filtering features, and ensuring mobile responsiveness.
Sprint 3: Focused on improving the user experience, adding admin features, and conducting extensive testing and bug fixes to ensure a smooth and reliable application.
Throughout the project, we used Jira to manage user stories, tasks, and epics, ensuring clear and effective communication among team members.

![image](https://github.com/omar7l/DorY/assets/115163722/a495a2a4-608f-4333-9965-7ad07650abba)

![image](https://github.com/omar7l/DorY/assets/115163722/e9d25e15-bc47-4a17-b9b5-e364bc852d01)

![image](https://github.com/omar7l/DorY/assets/115163722/4e26814a-ebe8-41a8-aa3f-4547b31ffead)

![image](https://github.com/omar7l/DorY/assets/115163722/7959e833-df97-4b00-a4ec-8232978fedbb)

![image](https://github.com/omar7l/DorY/assets/115163722/52883b6e-2409-4fff-b84b-f3df4940b48a)


### Roles
- Back-end developer: Omar and Emre 
- Front-end developer: Doris 
- Project Manager: Sarah  

#### Maintainer
- Omar Rahiel


