# cybuy - Software Architecture Document

## Table of Contents
1.	Introduction
    1.	Purpose
    2.	Scope
    3.	Definitions, Acronyms, and Abbreviations
    4.	References
    5.	Overview
2.	Architectural Representation
3.	Architectural Goals and Constraints
4.	Use-Case View
    1.	Use-Case Realizations
5.	Logical View
    1.	Overview
    2. Architecturally Significant Design Packages
6.	Process View
7.	Deployment View
8.	Implementation View
    1.	Overview
    2.	Layers
9.	Data View (optional)
10.	Size and Performance
11.	Quality

<br />
<br />

## 1.	Introduction
### 1.1	Purpose
This document provides a comprehensive architectural overview of the system, using a number of different architectural views to depict different aspects of the system. It is intended to capture and convey the significant architectural decisions which have been made on the system.

### 1.2	Scope
This document describes the architecture of the cybuy web marketplace.

### 1.3	Definitions, Acronyms, and Abbreviations
| Abbrevation | Description                            |
| ----------- | -------------------------------------- |
| API         | Application programming interface      |
| MVC         | Model view controller                  |
| REST        | Representational state transfer        |
| SDK         | Software development kit               |
| SRS         | Software requirements specification    |
| UC          | Use case                               |
| n/a         | not applicable                         |
| tbd         | to be determined                       |

### 1.4	References

### 1.5	Overview
This document details the thought process behind choosing the tech stack and tools for the cybuy projects, architectural freedoms and constraints as well as the implementation and deployment stemming from the prior.


## 2.	Architectural Representation 


## 3.	Architectural Goals and Constraints 
All the following decisions were made based around Modifiability since we deemed it very important:
-	Striving for an MVC style backend by using Java Spring Boot connected through REST APIs
-	Striving for a clean component based approach with separation of View and Business logic using Angular as the frontend
-	Modulithic design for faster development allowed by limited target audience and thus lower amount of required scalability
-	Easily bootable in a test environment consisting of an IDE, JDK, NodeJS install with light amount of npm command knowledge and a containerized test database (OS agnostic stack)
-	Containerized test database provides test data and saves time during testing
-	Git is used to hold snapshots of working code states and allows rollbacks during development
-	Likewise the database is subject to periodical backups to allow reversion in event of unforeseen failure

## 4.	Use-Case View


### 4.1	Use-Case Realizations


## 5.	Logical View


### 5.1	Overview

### 5.2	Architecturally Significant Design Packages


## 6.	Process View 
Examples of light weight processes with high importance:

![Sequence Diagram Account Creation](/resources/sequence_diagrams/SequenceDiagramAccountCreation.png)

![Sequence Diagram Logging In](/resources/sequence_diagrams/SequenceDiagramLogginIn.png)

## 7.	Deployment View 
 
## 8.	Implementation View
![Package Diagram](/resources/PackageDiagram.png)

The backend package diagram is constructed using the decomposition structure.
This is due to the fact that our frontend is written in TypeScript and accesses the backend via API calls. Since every page requests at least some data from every controller the other structures were out of the question and are generally better suited to, for example, all JavaScript based approach akin to NodeJS projects.

## 9.	Data View (optional)

## 10.	Size and Performance

## 11.	Quality 
We chose to focus our software architecture on modifiability. Since we rely on a modulithic approach we have made plans to arrange for an easy to use testing environment on the same machines development takes place on. The difficulty arises in the rollout phase of the update, but even so thanks to the vision of the site not including time sensitive actions such as auctions allows us to schedule downtime and to apply all patches to production. 