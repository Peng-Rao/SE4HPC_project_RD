# Goal and approach

The objective of this project is to apply in practice what you have learnt during the first part of the course about requirement engineering and design.

The exercise consists in analyzing the problem presented in the following section and in writing a document (in Section 5 we provide some suggestions on the structure of this document) including the following elements:

Requirement analysis aspects: Derive from the goals in the problem description the use cases, requirements (both functional and non-functional), and domain assumptions. For brevity, you do not need to describe in detail each individual use case. One or more use case diagrams and the detailed description of the use case you feel is the most critical/important will be enough. Don’t forget to take into account all relevant actors in the considered domain. Remember that actors are not only human beings, but all relevant devices/legacy software that interact with your system and play a role in some use case.

- Architectural design: Define the architecture for your system. Use component diagrams and sequence diagrams to present the architecture. Describe the purpose of each component. Highlight in the sequence diagrams how components interact with each other. Discuss about the criticalities behind your system and how you plan to address them.

# Steps and deadlines

Group registration: fill in the form https://forms.office.com/e/NGGC9VVJVb. Deadline: 31/03/2025  
Document submission: upload your document here https://webeep.polimi.it/mod/assign/view.php?id=334529. Deadline: 23/04/2025 Feedback by instructors due by 12/05/2025

# Rules

- Groups can be composed of two to four students each. If a student, for any reason, is aware of not being able to coordinate with others and, therefore, be part of a group, can take the project as an individual. This, however, should be considered as the last resort as the work of a software engineer is inherently collaborative and takes

- advantage of the discussion with multiple stakeholders. For this same reason, larger groups are preferable.

- You must provide the requirement and design document within the stated deadline. A delay of a few days, if notified in advance to the reference professor, will be tolerated, but it will also result in a penalty in the final score.
- The maximum score for this assignment is 8 points. The assessment will be based on the accuracy, consistency, and completeness of the requirement and design parts.

# The problem

Two urgent global concerns are environmental sustainability and climate change; because of air pollution and greenhouse gas emissions, transportation—especially urban commuting— contributes to worsening those issues.

To reduce the impact of urban commuting, we want to keep it under control with the following types of actions:

- Type1: We want to dynamically modify the duration of traffic lights on the main roads in the city depending on the directions from where we observe the main traffic movements. For instance, if, at a certain point in time, we observe that the traffic flow on a certain road A is significantly higher than in the crossing roads, then we may decide to extend, for instance, for one hour, the duration of green lights on A (and, consequently, extend the duration of red lights in the crossing roads).

- Type2: We want to analyze the daily traffic patterns and identify possible optimizations in terms of one-way roads, traffic lights configuration, and public transport schedule.

- Type3: We want to collect information about the planning of events attracting large crowds (e.g., important sport events, concerts, fairs) and define event-specific configurations for traffic lights, roads and public transport schedules.

To accomplish these goals, we can rely on the following elements:

- A preexisting infrastructure offering sensors that measure the number of seconds cars need to cross each intersection. This infrastructure is developed according to the event-based style. All sensors periodically publish the data they have acquired on a message bus.  
  A microservice offering information about public transport schedules. In particular, this microservice is offering the following operations: o getScheduleByStreet: Given the name of a street, it returns the timetable of all stops present on that street. o getScheduleByLine: Given the number of a specific line, it returns the complete timetable for that line.

- A news channel that transmits information about the events in the city as soon as they are planned.

- The project “SustainCity” aims to create a comprehensive software system that integrates the sources of information listed above, automatically applies actions of Type1, and provides suggestions to the urban area managers for what concerns actions of Type2 and Type3. The software should also log all actions of Type1 actuated. Moreover, it should publish for all citizens the following reports:

- Daily reports about the average traffic flow on the main roads and about the Type1 actions taken. Yearly reports about the actions of Type2 and Type3 suggested and not accepted by the urban area managers and those suggested and accepted.

Assignment for groups composed of two students and for individuals: please focus your requirement analysis and design work on the features in the description related to actions of Type1.

Assignment for groups composed of three students: please focus your requirement analysis and design work on all the features in the description related to actions of Type1 and Type2.

Assignment for groups composed of four students: please focus your requirement analysis and design work on all the features in the description.

# The document to be created

The document you produce will include at least the following elements. You can extend this structure if you think it is needed:

- A front page that includes the project title (it is up to each group to invent a name for it), the version of the document, your names and the release date.
- A table of contents that includes the headers of the first three levels of headings in your document, with the corresponding page number.
- Section 1. The project and project goals. You can copy and freely re-elaborate (if needed) the description you find in this document. 
- Section 2. Requirement analysis. It will include:  
  - Relevant human and non-human actors 
  - Use cases o 2.3. 
  - Domain assumptions o 2.4. 
  - Requirements 
    - Functional requirements
    - Non-functional requirements 

Design. It will include:
- General description of the architecture. It will include a component diagram and a description of components.
- Sequence diagrams. Include here at least three sequence diagrams that describe the most relevant interactions in the system.
- Critical points and design decisions.
