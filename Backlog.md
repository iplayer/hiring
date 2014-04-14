# Coding Exercise

Your team has been asked to create an Agile/Scrum task tracking system. This web system will allow the entire BBC to use this tool to manage their team’s backlog, and every employee will have access to it. 

You are part of the backend web service team, and are responsible for implementing a RESTful micro-service that represents the backlog. The REST service will have the following APIs:

### /backlog
* GET /backlog
  * List the stories in the backlog in priority order.
  * Returns 200 if a list of stories is retrieved.
* GET /backlog?points=:estimatedTotal
  * List all stories in the backlog (in priority order) that can be done given estimated total number of points that can be done.
  * Returns 200 if a list of stories is retrieved. Returns 400 if estimatedTotal is negative, 0, or not a number.
* POST /backlog
  * Add a new story to the backlog. 
  * Use Story JSON format below.
  * Returns 200 if the story is added. Otherwise standard HTTP error code is returned.
* GET /backlog/story/:id
  * Get a story with the unique identifier provided.
  * Returns 200 if the story is retrieved. If the story with that identifier does not exist, then returns 404.
* PUT /backlog/story/:id
  * Update the story with the unique identifier provided. Use Story JSON format below. 
  * Returns 200 if the story is updated. Otherwise standard HTTP error code is returned.
* DELETE /backlog/story/:id
  * Remove a story from the backlog using the identifier provided.
  * Returns 200 if the story is removed. Otherwise standard HTTP error code is returned.

```javascript
{
   "id": 123,
   "points": 8,
   "priority": 1,
   "title": "Style the iPlayer icon to be more pink."
}
```

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
