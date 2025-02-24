## Introduction
This page will provide a continuous overview of the current project.  It is not intended to replicate or negate the need for a full architectural cycle, but should be seen as an ‘architecture-light’ process that allows the reader to see an up-to-date and clear overview of the deliverable.

The following pages will explore the scope and requirements in ever-increasing detail, and as such, will become siloed within there relevant sections.  This page will provide a clear overview of the bigger picture whilst leaning on the  TOGAF/Architectural principles. 

### Project Statement
HillsHealth.org is an online site built in 2012 which contains a number of summarised health and medical trials covering 9 key topics.  The as-is process needs to be extended to allow for automated systematic reviews, an extractive summariser, and video output.

### Business Context
HillsHealth.org currently provides ~500 summarised and paraphrased medical trials covering a range of key health subjects.  The objective is for these past-learnings to be the foundation of an extended eco-system that covers published health and medical journals, and how these peer-reviewed trials support or oppose current GP prescription data, current health spending, wider population health statistics, and specific health concerns.  These new deliverables will be provided through online media and through enhancements to the current HillsHealth.org domain.

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/87730072-b275ce00-c7be-11ea-954e-f1146c5b54ca.png" width="500" height="500"></p>

The assumptions of the eco-system are that the following are included:
* It is assumed that access to evidence-based medicine/health is available.
* It is assumed that access to GP prescription data and population health statistics is available.
* It is assumed that, where possible, the end-to-end process is automated.
* The delivered content is freely available.
* It is assumed that integration within the eco-system is scalable and seamless.

### Problem Definition
Peer-reviewed health and medical research needs to be available to a non-academic audience and presented in a succinct and contemporary manner.  Furthermore, prescription, health spending, and general population health statistics should to be held up scrutiny with an emphasis on the latest and best available research.

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/82125670-5b905000-979f-11ea-80f1-6ce00096a2ac.png" width="350" height="350"></p>

## Design Principles and Approach
The Architecture Development Method (shown below) is a detailed step-by-step process for implementing change and development. The ADM helps to develop processes that involve multiple check points and firmly establishes requirements.

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/117441542-710d0580-af2d-11eb-9082-a681ffa765bd.png" width="400" height="400"></p>

### 1. Preliminary
#### Objectives
The current hillshealth.org solution is limited to manually generated abstractive summaries. This is a 1-to-1 approach where one article represents a single medical trial. An enhanced solution is required that will complete a systematic review of the primary medical trials on a given subject and produce a system generated abstractive/extractive summary.  This summary will be presented in a short video format.

As a private project there will be no external stakeholders involved.  Software resources are required as are licences to several software suites including Adobe CC and Azure.

The key driver for this piece is to enable users to source the gold-standard of health information in a way that is engaging and easily understood.  There is no particular framework to be followed and no sponsor.  Furthermore, as a private project, there are no human resource needs, no commercials, cultural aspirations or strategic intent, no change management process, definition of done or specified framework (i.e. Agile / Lean).

#### RACI

| Responsible <img width=100/> | Approver <img width=100/>| Consulted <img width=100/>|
| ------------- | ------------- | ------------- |
|... |... |... |
|... |... |... |
|... |... |... |


<img src="https://user-images.githubusercontent.com/45914355/82615061-57aa6680-9bc1-11ea-9314-b15c51ac02f9.png" width="400" height="400">


#### Capability and Approach
This deliverable must establish a solution that is capable of generating a summary of a group of medical trials on a given topic/question, or more simply, produce a systematic review.  The solution will search using publicly available medical databases (PubMed, PubMed Central, Embase) and collect trials from open-access and subscribed providers.  Keywords and text will be extracted from the papers and a quality score produced.  The keywords and text from papers of a suitable quality will provide the content for a systematic review.  The output from the systematic review should answer the initial question through a short video or infographic.


### 2. Architecture Vision (Business Outcome)
#### 1. Literature Search and meta-analysis
A specific health question or topic will be searched via a health database (PubMed, PubMed Central, Embase).  The results returned will be filtered to include only those that meet a set criteria and therefore a certain level of quality.  The chosen papers will form the basis of a systematic review that will produce an overall outcome or opinion. 
#### 2. Abstractive Summarisation
The output of the systematic review will be analysed and a summary produced.  This will be a system generated abstract and will cover; a) participants, b) study, c) results, d) conclusion.
#### 3. Video output
The results of the abstractive summary will be the basis for a short video which will be posted online.

How does the vision meet the goals, objectives, and stakeholder concerns/problems
Include a process map/business model here to how this will deliver the goals/strategy to stakeholders and customers.

#### Vision
The vision for the deliverable is to:

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/87787816-2900e300-c834-11ea-9158-904cc66d89bf.png"></p>

* MVP: Publish summaries of EBM to a non-academic audience via contemporary methods.

* Non-MVP: Use published medical research and scientific study to consider question published health statistics e.g GP prescription data.

![Functional view (2)](https://user-images.githubusercontent.com/45914355/82125071-3863a180-979b-11ea-8f3f-a9e571aceab5.png)

#### Functional View

The deliverable is primarily a graphic component relying on EBM and publicly available health statistics.  It will be an integral component to search for relevant and qualitative EBM, extract the relevant points from the EBM, summarise the EBM, present this data, and to further use the results to question population health statistics.

*Functional view TBC*

#### Scope

The solution intends to deliver the following goals and principles for the platform

G1: Based on a given question, topic or finding, search medical databases in order to return relevant papers.

G2: Filter medical papers to produce a list of primary sources.

G3: Extract keywords and text from the primary sources.

G4: Create a quality score of the primary sources.

G5: Create an automated systematic review of the primary sources.

G6: Consider the output of the systematic review against current U.K GP prescription data.

G7: Display the output online via a short video or infographic.

P1: Ensure the medical summaries are a fair representation of the source

P2: Ensure the output is unbiased, and where possible, contains minimal editorial re-write.

P3: Strive for automation of the summary, paraphrasing, and graphical output.

P4: Reference the source paper.


#### Dependencies

Access to medical papers and official health data (NHS GP prescription data)

#### Goals

Goals are defined in two perspectives; firstly, the immediate goals of this work; secondly, the goal that is enabled on a successful outcome of this work.

##### Goals for this Work

In this work, we will build a systematic review of EBM that is automated and will target key health topics. It will generate an summary of the collated papers and create a visualisation that will be posted online.

The development journey will also look to encompass the latest ML and analytic methods through the use of journal data to evaluate GP prescribing trends.

Finally, despite not forming part of the MVP, narrative information should be sought through doctors and patients which allow us to analyse the richness of their accumulated experiences.

##### Goals beyond this Work

A successful outcome of this work will enable expansion into further areas of health and medical research, and present complex medical information in a simplified yet targeted manner. The goal is to provide the 'gold standard' of health and medical information, namely peer-reviewed medical trials, to a non-academic and online audience.

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/87732680-99bce680-c7c5-11ea-88cf-fea52a00be60.png"></p>

#### Out of Scope

N/A.

The scope model below shows which system features are in-scope (inside the boundary) and which ones are out of scope (outside the boundary).  

<p align="center"><img src="https://user-images.githubusercontent.com/45914355/87785938-fdc8c480-c830-11ea-9d59-5b3cfbfacb03.png"></p>

#### Critical Success Factors

* CSF01: Automation -The deliverable must be able to search, return and grade the quality of medical papers.

* CSF02: Data accuracy - The deliverable must be able to produce a summary of the returned papers.

* CSF03: Content Delivery - The output must be presented via video.

* CSF04: User engagement - The deliverable must be clear and offer customers an easy to understand solution.

* CSF05: Increase in user metrics - Increase in views (metric TBC)



### 3. Business Architecture (existing and proposed)
Objectives… consider
Develop target architecture.
Identify architecture roadmap that is gap analysis
Relate business elements to business goals

Output… consider
Apply business capabilities - views of business as shown in phase A should be mapped to units, value streams, info systems, strategic plans.
Apply value streams - inform SH about business capabilities.
Apply org map - who to involve
Apply business modelling - activity models, UC, class diagrams etc.

#### Existing Registration and Login Architecture
#### Proposed Business Journey (Process Map)
#### Proposed Business Journey (Process Model)



### 4. Information Systems & Data Architecture (existing and proposed)
Objectives… consider
Develop information systems architecture
Develop target info systems.
Identify architecture roadmap that is gap analysis
Relate business elements to business goals

Output… consider
Data management - standards for software, how data entities utilised/created/stored, data transformations, software needed.
Data migration - requirements including cleaning and transformation. Establish data definition.
Data governance - structure of organisation relevant to transformation, management systems, people skills.

#### System Use Cases

System use cases will document how the abstractive summaries interact with other components in the eco-system.

System use cases are generally documented using a single use case diagram with different component boundaries defined.  At this level, details with the use case will not be defined or examined.

The system use case diagram below documents the known use case for the deliverable, the interaction across the eco-system, and use case journey through the system components.

<img src="https://user-images.githubusercontent.com/45914355/82714358-19c34600-9c86-11ea-8810-49ef3eec05fb.png" width="850" height="850">

#### HL Activity View

![Process Overview](https://user-images.githubusercontent.com/45914355/85082902-22953200-b1c8-11ea-8064-19a9aff0e8e7.png)


#### Conceptual Data Model

Below is the draft conceptual data model for the deliverable.  This model is intended to show core entities and their relationships and dependencies.  The model also shows relationships to other data sets within the eco-system e.g prescription and population data.  This will take a more detailed shape and will be input for the logical data model as more requirements and to-be business processes are documented.

_...data flow diagram to be added here_
 
_...logical data flow model to be added here_

#### Data Quality and Timeliness
##### Volumes

The numbers of abstractive summaries produced, and subsequent visualisations, has not been determined at this time.  Capacity is dependent upon the strength of the model produced, and any subsequent editorial re-write.

##### Transactional Management and Recovery

_...sequence diagram to be added here_

##### Ownership and Governance

Unlike standard architecture practice, ensuring the complete follow through of the data will remain the responsibility of the owner.

##### Data Lifecycle

The details below will be added following development of the models





### 5. Technology Architecture
Objectives… consider
Develop target tech architecture that enables architectural vision and deliver building blocks through tech that addresses SoW.
Identify architectural road map based on gaps.

Output… consider
Transformation opportunities.

#### Application View

##### Packages and Components

--The following component diagram is a place holder and needs updating
![Component Diagram (6)](https://user-images.githubusercontent.com/45914355/87832274-8bca9c80-c87d-11ea-95e4-3526092db0ed.png)

##### Interfaces

_Upstream solutions provide data to this solution, downstream solutions receive data from this solution.  Solutions may be both upstream and downstream.  Interfaces should be categorised as interactive or bulk and the transfer mechanisms described._

###### Upstream Dependencies

Pubmed.gov will be the primary search tool for journal citation.  An API will search and retrieve the links to the full text articles.  There is no intention to use abstract only papers which would not allow the strength of the paper to be measured or allow for an accurate summarisation of the data.

If available, direct access to journal sites may be required where a) costs permit, and b) it is felt that the topics covered are current and in the immediate public interest.

Open access data sources will provide input to the deliverable and allow analysis against trial findings.  In all instances, upstream data sources will be referenced and hyperlinked. 

###### Downstream Dependencies

No project is dependent upon completion of this deliverable. However, social media and an individual online presence will receive data from this solution.  The online presence will utilise either the hillsHealth.org or hillsHealth.co domain, and this WFE will be a point of access to the solution that is both searchable and customisable.



### 6. Opportunities and Solutions
Objectives… consider
Group work into packages
Perform initial implementation planning
Decide on approach - make vs buy vs re-use.
Asses priorities and identify dependencies.
Develop complete architectural road map
Roadmap to deliver continuous value.
Define solution building blocks.

Output… consider
How to deliver architecture. Four components in transition to deliver target; architecture roadmap, work packages, transition architecture, implementation and migration plan.
Architecture roadmap lists work packages on timeline.


### 7. Migration Planning
Objectives… consider
Provide cost/benefit and risk assessment

Output… consider
Assess dependencies / costs / benefits.
Define Business value
Create implementation an migration plan.


### 8. Implementation Governance
Objectives… consider
Monitor ongoing work and implementation

Output… consider
Phased deployment schedule.
Ensure compliance with defined architecture

#### Deployment Approach
##### Approach

The deployment approach for the solution will consider the following approach to delivery:

* SaaS IaaS (PaaS will form part of the long term strategic view)

##### Technology Dependencies

* Development – Python and relevant libraries (NLTK)

* Storage – Azure Blob Storage, Azure SQL, Azure DF

* Statistical Software - SKLearn, matplotlib, 

* Visual – Adobe CC

##### People and Skill Dependencies
##### Environments

##### Automation and Operations
##### Sizing and Capacity

#### Setup and Maintenance
##### Migrations

#### Monitoring
##### Availability, Resilience and Recovery
##### Planned Downtime
##### Unplanned Downtime
##### Disaster Recovery

#### Security View
##### Approach
##### Implementation

#### Geospatial View
##### Approach
##### External Dependencies

#### Social View
##### Approach
##### External Dependencies

#### Legal and Compliance View
##### Statutory Regulation
##### Privacy and Data Regulation

#### Accessibility View
##### Approach
##### External Dependencies



### 9. Architecture Change Management
Objectives… consider
Manage change to deliverables / scope creep

Output… consider
Impact assessment, resource allocation, assessment.
Change management or redesign required


### 10. Requirements Management
Objectives… consider
Identify requirements and feeds in and out of relevant phases
Manage requirements as they enter the sprint

Output… consider
Deal with changes to 'requirements for requirements'.
Look after requirements (and consider dependencies or OTS solutions)
