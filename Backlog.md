# Coding Exercise

Your team has been asked to create an Agile/Scrum task tracking system. This web system will allow the entire BBC to use this tool to manage their team’s backlog, and every employee will have access to it. 

You are part of the backend web service team, and are responsible for implementing a RESTful micro-service that represents the backlog. The REST service will have the following APIs:

## /backlog
|------|--------------------------------------------------------------|
| GET  | List the stories in the backlog.                             |
| POST | Add a new story to the backlog. Use Story JSON format below. |

## /backlog/story/:id
|------|--------------------------------------------------------------|
| GET  | Get a story with the unique identifier provided.             |
| PUT  | Update the story with the unique identifier provided.        |
|DELETE| Remove a story from the backlog.                             |



- Each Story class has 
  - `Id` which is a __unique__ identifier for each story,
  - `Points` which represents an estimate of development effort required to complete the story,
  - `Priority` which represents the business priority of the story. *Lower numeric value implies higher priority*, for example, a Story with Priority = 1 is more important than a Story with a Priority = 3. 
- The `getSprint(totalPointsAchievable)` method of the Backlog class should return a list of `Story` in the order of business priority, based on the number of points each story takes and the given `totalPointsAchievable` in a sprint.
- You are free to change the instance variable types if necessary.
- You may implement your solution in any appropriate (i.e. non-obscure) language, and you may choose to implement the storage of any relevant data structures in memory or using a database, but please make sure your solution is working end-to-end and you include instructions for us to run and test your code.
- You should consider how concurrent use of the system may impact your implementation.
- Your response will be evaluated against four key criteria:
  - Design, Modularisation and Componentisation
  - Testing Approach and Scenarios
  - Concurrency and Performance
  - Style and Readability
