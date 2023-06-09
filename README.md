![visitors](https://visitor-badge.glitch.me/badge?page_id=page.id) 
[![](https://tokei.rs/b1/github/XAMPPRocky/tokei)](https://github.com/InnopolisUniversity/innometrics-dashboard/edit/master).
![GitHub issues](https://img.shields.io/github/issues/shaxri/NlpWithNeuralNetwork)
![Website](https://img.shields.io/website?up_color=red&up_message=Online&url=https%3A%2F%2Finnometrics.ru%2F%23innometrics-subscribe)
![GitHub forks](https://img.shields.io/github/forks/shaxri/NlpWithNeuralNetwork?style=social)
<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/xavzelada/https://github.com/InnopolisUniversity/innometrics-java-backend">
# Innometrics 

## Project description

The Innometrics application focuses on the collection of various process-related metrics in software development. 
Metrics such as tasks performed by the user, and the time and number of resources used to perform the activity used in a 
project, all metrics are stored locally. The main principles of the project are scalability, fault tolerance and 
adaptability to new requirements. 

The container diagram below shows the high-level shape of the software architecture and how responsibilities are distributed across it. 
It also shows the major technology choices and how the containers communicate with one another.

![img][https://github.com/aldeeyar/innometrics-info/blob/main/images/container_diagram.png]

In order to provide a system with such capabilities, a backend based on microservices 
has been developed. The backend consists of a number of specialised services, each responsible for a different part of 
the system, all communicating via a well-defined API. The backend schema is provided below 

![c4.jpg](images%2Fc4.jpg)

Backend consist of 5 microservices: 

### Authorization service

This is a component specialised in authenticating and authorising users, as well as generating and validating the 
tokens needed to process each request handled by the different services within the system. 
The JSON Web Token technology is used for this purpose.

### Configuration service

This service provides the functionalities that allow the administrator to make configurations within the system, such as 
user and role administration, and configure the rate with which the data analysis activity is executed.

### Rest-API service

The Data Collection API provides a communication interface to the various data collection modules. 
It is the entry point for the request. The Rest API service validates the requests.

### Activities-collector services

To be able to extract information on the collected data, a process will be developed that will be responsible 
for carrying out the data transformations that are necessary to carry these data from a scheme concerning an 
information model more suitable for end users.

### Agent-gateway service

The agent-gateway service focuses on metrics aggregation and storage. It is an automatic data transformation module, 
which takes the raw collected data and transforms them to perform an analysis process. It aims not to affect the 
performance of the transactional database during data processing.

## Frontend

In the frontend part we have some data structures, such as company, agent (integration), and GQM model. 
Agent is a service collecting data about user behaviour on predefined metrics. Company creates a company 
where a user can connect monitoring of agent metrics, as well as add team members. To create a connection between
agents and companies there is an integration service. One integration can have several metrics on how to obtain data. 
GQM helps to estimate which methods to use in integration based on user goal.

 ## Links

* [Dashboard](https://innometrics-12856.firebaseapp.com/#/login)

* [Frontend](https://github.com/InnopolisUniversity/innometrics-dashboard)

* [API](https://github.com/InnopolisUniversity/innometrics-backend/blob/master/documentation.yaml)
  (Access readable format by pasting `documentation.yaml` data to https://editor.swagger.io)
*  [Website](https://innometrics.ru/) 
* [Here](https://drive.google.com/file/d/1ghOf4uXLN9Nl4MYenroQuLhQ3GPfZMZW/view?usp=sharing) you can read about PRIVACY NOTICE of Innometrics system.


## Installation
[Here](https://github.com/aldeeyar/innometrics-info/blob/main/instructions.md) you can read the instructions for local running, automated deployment, and sonarcloud analysis.
