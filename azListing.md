# Coding Exercise
Your team has been asked to work with a new HTTP API that provides iPlayer with lists of programmes sorted alphabetically. Your task is to use the API to generate an A-Z listing for the website.

Each of the listing pages should include:

1. a list of programme titles and images
2. the ability to paginate if the letter has more than 20 results
3. navigation to other letters

## API
The API end point follows the following format:

```
{base_uri}/ibl/v1/atoz/{letter}/programmes?page={page}
```

| Parameter     | Value                              |
| ------------- | ---------------------------------- |
| `{base_uri}`  | The base server URI, which will be provided        |
| `{page}`      | page number to retrieve, from 1    |
| `{letter}`    | can be any single letter or `0-9`  |


## Notes
* You may implement your solution in any appropriate (i.e. non-obscure) language. But please make sure your solution is working end-to-end and you include instructions for us to run and test your code.
* Your code should be available on github or similar services with a full commit history.
* Although a fully working solution is desireable your response will primarily be evaluated against four key criteria:
  * Design, Modularisation and Componentisation
  * Testing Approach and Scenarios
  * Performance
  * Style and Readability
