---
title: Non Functional Requirements
description: Functional and non functional requirements for the solutions have affected the architecture decisions.
tags: [architecture]
weight: 6
linktitle: Non Functional
alwaysopen: false
aliases:
 - /architecture/
---

They are important input to deciding the Architecture Principles and Architecture Patterns. 

## Architectural Concerns
Architecture Concerns are categories of Non-Functional Requirements (NFRs) of a system that 
has been important defining this architecture. These are sometimes referred to as 
cross-cutting concerns or "the -ilities" because most of the words end with "-ility."

### Performance

#### Scalability
The platform need to be highly scalable. The traffic in this types of solutions involves a large part of the countries citizens and the traffic is often concentrated around a few dates.

#### Response Time
The solution need to have a performance to support a user friendly experience.

**Requirement:** Page load should be less than 1 second

#### Capacity

### Reliability

#### Availability
The solutions need to be available 24/7.

**Requirement:** The architecture itself needs to be able to support high availability. It can't require reqular downtime
or other maintainence that makes it not available. 

#### Recoverability
Based on the important of the solution the plattform needs to be recovorable also disaster events. 

**Requirement:** It should be possible to setup the solutions from scratch in xx hours (will be specificed)

### Security
Building a platform to host applications for different governmental agencies will involve sensitive data for citizens and businesses in the country. 

This makes security one of the most important architecture concern in the solutions. 

#### Authentication

#### Authorization

#### Single sign on

#### Isolation

#### Personel security

### Maintainability
The solutions will be open source and involve a large amount of developers. It is important that the different components are highly maintainable 
to support effective development


### Operability
The solutions will de operated by a small devops team and need to be highly operable. 
It needs to support automatic monitoring. 



### Usability

#### Accessibility
The applications running in the solutions will be accessed by all types of users and need to be following WCAG 


#### Localisation

### Portability


## Other Non Functional requirements

### System location
The Altinn solution needs to be located inside Norways borders. This requires that we only can choose amongst the cloud providers providing
cloud services inside Norway. 