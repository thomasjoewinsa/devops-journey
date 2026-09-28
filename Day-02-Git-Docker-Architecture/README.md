# Day 2 - Git, Docker and Software Architecture

## Topics Learned

* Git Clone
* Monolithic Architecture
* Microservices Architecture
* Introduction to Docker
* White Box Testing
* Grey Box Testing
* Black Box Testing
* Thread-Safe Files

## 1. Git Clone

`git clone` is a Git command used to copy an existing remote repository to a local computer.

### Syntax

```bash
git clone <repository-url>
```

### Example

```bash
git clone https://github.com/username/project.git
```

This command downloads the repository, including its files, commit history and branches, to your local machine.

## 2. Monolithic Architecture

Monolithic architecture is a software design approach in which an application is developed and deployed as a single unit.

### Characteristics

* All major components are part of one application.
* Components commonly share one codebase.
* The application is usually deployed as a single unit.
* Changes to one component may require rebuilding and redeploying the application.

### Example

An online shopping application where user management, product management, orders and payments are all developed as part of one application.

## 3. Microservices Architecture

Microservices architecture is a software design approach in which an application is divided into smaller, independently deployable services.

### Characteristics

* Each service focuses on a specific business function.
* Services communicate through APIs or messaging.
* Services can be developed and deployed independently.
* Different services may use different technologies.

### Example

An online shopping application with separate services for:

* User management
* Product management
* Order management
* Payment processing

## 4. Introduction to Docker

Docker is a platform used to build, package and run applications inside containers.

A container packages an application with its dependencies so that it can run consistently across different environments.

### Key Docker Concepts

* **Image:** A template used to create containers.
* **Container:** A running instance of an image.
* **Dockerfile:** A file containing instructions to build a Docker image.
* **Docker Hub:** A registry where Docker images can be stored and shared.

### Common Docker Commands

```bash
docker --version
docker pull nginx
docker images
docker ps
docker ps -a
docker run nginx
docker stop <container-id>
```

## 5. White Box Testing

White box testing is a software testing method in which the tester has knowledge of the internal code and program structure.

### Characteristics

* Tests internal logic and code paths.
* Checks conditions, branches and loops.
* Often performed by developers.
* Requires knowledge of the implementation.

## 6. Grey Box Testing

Grey box testing is a software testing method in which the tester has partial knowledge of the internal system.

### Characteristics

* Combines aspects of white box and black box testing.
* Uses partial knowledge of internal design.
* Can test interactions between components and data flow.
* Often useful for integration testing.

## 7. Black Box Testing

Black box testing is a software testing method in which the tester checks application functionality without needing to know the internal code.

### Characteristics

* Focuses on inputs and expected outputs.
* Tests application functionality against requirements.
* Does not require access to the internal implementation.
* Commonly used in functional testing.

## 8. Thread-Safe Files

Thread safety refers to the ability of code or a resource to be accessed by multiple threads without causing data corruption or inconsistent results.

When multiple threads access or modify the same file at the same time, synchronization or other coordination mechanisms may be needed to avoid conflicts.

### Common Techniques

* Locks
* Synchronization
* Thread-safe queues or file-writing services
* Controlled access to shared resources

The appropriate method depends on the programming language and the way the file is accessed.

## Key Takeaway

On Day 2, I learned how to clone Git repositories, understood the differences between monolithic and microservices architectures, explored the basics of Docker, learned about white box, grey box and black box testing, and studied the concept of thread safety.

**Status: Day 2 Completed**
