### Introduction
#### Document Purpose
This Document has a number of key purposes:
- To explain the need for this project to be progressed – the problem or opportunity.
- To understand any specific drivers or constraints that apply to the project and to justify assumptions on why IT and manual solutions are needed.
- To record the project objectives and high-level requirements (functional and non-functional).
- To establish and baseline the scope of the project, including in-scope processes and classes of data.

This document will NOT describe a solution.  In particular, requirements should not mention specific IT applications, components or interfaces between them.  Those things however could be mentioned in accompanying information such as background information etc. where appropriate.

#### Target Audience
All business and IT stakeholders.

### Business Context
#### Project Background
There is no main-stream online resource available to present medical research to a non-academic audience.  Users are therefore reliant on the abundance of opinion and hear-say when seeking answers to their health and medical questions.  

A solution is required that will produce abstractive summarisations on a number of key health topics.  It is envisaged that the reviews will be presented via a short video through social media.  The process will need to be automated where possible with limited manual intervention or re-write.  

Following the launch of HillsHealth.org in 2012, this current project will automate what was previously a manual solution, and deliver the summaries in a contemporary and salient manner.

#### Problem/Opportunity Statement

The volume of fake and mis-leading online articles covering health and medical opinion makes it difficult for the user to differentiate fact from fiction.  Trials published in medical journals are the gold-standard of health and medical information and should be accessible to all.  However, the academic slant of these papers make them incomprehensible to the non-scholar, and with a pay-wall preventing full access to all but a few sites, a solution is required to bring the information to the layman and provide an on-line audience with a better alternative to the current volume of mis-leading, and often dangerous, medical and health information. 

This project will look to enhance the on-line experience by giving users access to evidence-based medicine and health information that is aggregated, summarised and paraphrased.  The solution will engage the user via social-media and provide the summary via short on-line video or infographic.  Output is expected to be automated with limited manual review.  This will allow for a greater volume of articles that is currently possible via the current HillsHealth.org site.


### Business Objectives
|Ref | Title |Description |
|---|---|---|
|BOJ01 |Process Optimisation |	Automate the summary of medical papers from scientific journals <img width=500/>|
|BOJ02 |Content Aggregation| Group together relevant and similar medical papers|
|BOJ03 |Source Scoring | Score the quality of the journal and the paper|
|BOJ04 |Content Production | Present systematic reviews in a contemporary, clear, and eye-catching manner|
|BOJ05 |Content Delivery| Use online media to deliver summaries to the wider audience| 


### Critical Success Factors
|Ref |	Title |	Description |
|---|---|---|
|CSF01 | Automation | The deliverable must be able to summarise and paraphrase medical papers. <img width=500/>|
|CSF02 | Data accuracy | Summaries must accurately reflect the source paper.|
|CSF03 | Quality score | The quality of the source paper must be scored based on established criteria.|
|CSF04 | Content Delivery | The output must be presented via motion graphic|
|CSF05 | User engagement | The deliverable must be clear and offer customers an easy to understand solution.|
|CSF06 | Increase in user metrics | Increase in views (metric TBC)|

### Key Assumptions
- Access to medical journals is available.
- No project timescale applies.
- Resource is available for all aspects of the project.
- Funding is available for the project.

### Drivers and Constraints
Scope -  The project needs to automate the aggregation and summary of medical papers and present the output via an online video

Quality – All requirements must be well defined to facilitate the build quality of the design.

Time – The project must go live on (date TBD)

Cost -  Funding is available for all elements of the project


|Driver <img width=75/> | Descriptions of importance or any constraints that are relevant <img width=500/> | Priority
|---|---|---|
|Time |	Earliest possible delivery |3 |
|Cost |	Within funding budget | 4 |
|Quality | Summaries must be of a quality that adds value to the customer’s experience |2| 
|Scope | Provide a summarised systematic review of medical papers and publish online | 1 |

### Definition of Scope
#### Processes
|Processes|Description of Impact|
|---|---|
|Data Mining | Extract medical papers from scientific journals specific to a chosen topic.|
|Natural Language Processing | Transform the medical papers to a summarised and paraphrased review. Reviews should be a handful of key points covering participants, study and results.|
|Source Quality| Score the Journal (impact factor) and quality of the paper (Jadad scale) and present the score with the final output.|
|Systematic Review| Papers that meet a suitable criteria and score will be aggregated and overall outcome produced|
|Data Presentation| The output from the systematic review, with scoring, should be presented via an online video|
|Manual Sanity Check| The editor will review the outcome for accuracy and suitable presentation|
|Summary Posted | The summarised and paraphrased graphic will be posted to a suitable online site|

Process Map (draft) of the proposed solution can be found below:

![Process Overview](https://user-images.githubusercontent.com/45914355/85082902-22953200-b1c8-11ea-8064-19a9aff0e8e7.png)

#### Customer Segment
|Customer Segment| Description of Impact|
|---|---|
|All|The output should be universally available via social media and will cover the following key health topics; Diet & Nutrition, Sports & Exercise, Cardiovascular & Stroke, Complementary Medicine, Diabetes, Cancer & Oncology, Pregnancy & Paediatrics, Elderly and Rheumatology, Dating and Happiness.|

#### Out of Scope

Updating the 'as-is' WFE of HillsHealth.org (phase 2 : non-MVP)

Posting the output of this deliverable to HillsHealth.org (phase 2 : non-MVP)

Prescription data, population health statistics, and health spending as a reflection of evidence-based medicine (phase 2 : non-MVP).

Narrative evidence analysis via annonymous patient and doctor experinces or case studies.  

### High Level Requirements
#### High Level Functional Requirements
|Ref| Title| Description| Priority (MSC)|Related Req(s)|
|---|---|---|---|---|
|FR01|	Data Mining| Data Mine relevant articles from a selection of medical journals.  The chosen journals will be based on their impact factor, with papers chosen from the range of key health topics as described above and validated against an extended Jadad criteria.|	M|	UC-01|
|FR02|	Article analysis and refinement|	A solution will summarise and paraphrase the articles provided in FR01.|	M|	UC-|
|FR03|	Journal and paper quality score|	A solution will search the paper and provide a quality score based on a pre-set criteria.  Journal quality to come from the impact factor.|	S|	UC-|
|FR04|	Create Systematic Review|	A solution that will create an aggregated output of the summaries created in FR02|	M|	UC-|
|FR05|	Create Summary Visualisation|	A solution that will enable the systematic review created in FR04 to be visualised|	M|	UC-|
|FR06|	Post summaries on-line|	The FR05 output will be posted on-line |	M|	UC-|

### High Level Data Requirements
|Ref|	Title|	Description|	Priority (MSCW)|	Related Requirements|
|---|---|---|---|---|
|DR01|	Customer Logins|	Summaries must reflect the information provided in the journal paper.|	M|	FR00|
|DR02|	|	|	|	|


### High Level Non-Functional Requirements
|Ref|	Title|	Description <img width=300/>|	Priority (MSCW)|	NFR Type|	Related Req’s|
|---|---|---|---|---|---|
|NFR01|	Algorithm|	Timely response to request for summaries|	S|	Performance – Speed|	FR01|
|NFR02|	Summaries|	24/7 availability (both input and output)|	S|	Availability - Hrs|	FR01|
|NFR03|	User|	Enhanced visual impact|	S|	User Impact	| |
|NFR04|	Automation|	Minimal manual input|	S|	Disruption|	|
|NFR05|	L & R|	Compliant to all L & R requirements|	M|	Legal and Regulatory|	FR01|

### Potential Extent of IT solution

### Naming Conventions
|Term| Description|
|---|---|
|TBC| TBC|
