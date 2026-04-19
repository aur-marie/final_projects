# final_projects
First Project Java Spring
A beginner Spring Boot web application built with Java and Thymeleaf, developed as part of coursework at Vistula University.

 Project Overview
This project demonstrates the basics of building a web application using Spring Boot. It includes a simple controller that handles HTTP GET requests and renders dynamic HTML pages using the Thymeleaf templating engine.

 Project Structure
first-project-java-spring/
├── src/

|  └── main/

|      ├── java/

|      └── pl/edu/vistula/first_project_java_spring/

│             ├── FirstProjectJavaSpringApplication.java 

│                  └── controller/

│                        └── HelloController.java 

│         └── resources/

│           └── templates/

│               └── greeting.html    

└── README.md


 Getting Started
 
Prerequisites

Java 25

Maven 

An IDE used is IntelliJ IDEA 


Running the Application


Clone the repository:


bash   git clone <your-repo-url>

   cd first-project-java-spring
   

Build and run using Maven:


bash   mvn spring-boot:run


Open your browser and navigate to:


   http://localhost:8080/
   

Endpoints

MethodURLDescriptionGET/Returns a plain text hello messageGET/greetingRenders a greeting page with an optional name parameter

Example Usage


Default greeting:


  http://localhost:8080/greeting
  
Displays: Hello, World!


Custom greeting:


  http://localhost:8080/greeting?name=Vistula
  
Displays: Hello, Vistula!


Technologies Used


Java — Core programming language

Spring Boot — Application framework

Spring MVC — Web layer / controller handling

Thymeleaf — Server-side HTML templating engine

Maven — Build and dependency management



 Key Files
 
FirstProjectJavaSpringApplication.java

The main entry point of the application. Uses the @SpringBootApplication annotation to enable auto-configuration and 

component scanning, then launches the embedded web server via SpringApplication.run().

HelloController.java

A Spring MVC controller (@Controller) that handles two routes:


/ — returns a plain text greeting string.

/greeting — accepts an optional name query parameter (defaults to "World"), adds it to the model, and renders the 
greeting.html template.


greeting.html

A Thymeleaf template that dynamically displays the greeting message using the name attribute passed from the controller.
Also displays the Vistula University logo.

