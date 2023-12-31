# Dancing in the Stars Documentation

## Server API Endpoints

  | METHOD | ENDPOINT             | USAGE                       | RETURNS                          |SENDS        |
  | ------ | ---------------------| ----------------------------|----------------------------------|-------------|
  | GET    | `/v1/dances`         | Get a list of dances        | An array of dances               | nothing
  | GET    | `/v1/dances/:id`     | Get a dance object by id    | A specific dance object          | nothing
  | GET    | `/v1/dances/complete`| Get the isComplete field    | An array of boolean              | nothing
  | PATCH  | `/v1/dances/:id`     | Update the isComplte field  | The updated boolean value (true) | {isComplete: X}

## Post Endpoints

### Get Dances

  Request type and route:<br />
  **GET `/v1/dances`**

  Response:

  ```json
  [
    {
      "id": 1,
      "name": "Orange Justice",
      "isComplete": false,
      
    }
  ]
  ```

  ### Get Dances by Id

  Request type and route:<br />
  **GET `/v1/dances/:id`**

  Response:

  ```json
  
    {
      "id": 1,
      "name": "Orange Justice",
      "description": "blah blah blah",
      "link": "youtube url",
      "isComplete": false,
      
    }
  
  ```
### Get Count

  Request type and route:<br />
  **GET `/v1/dances`**

  Response:

  ```json
  [
    {
      "isComplete": false,
    }
  ]
  ```


### Update Dances (isComplete)

  Request type and route:<br />
  **PATCH `/v1/dances/:id`**

  Request body:

  ```json
  {
    "isComplete": false,
  }
  ```

  Response:

  ```json
    {
      "id": 1,
      "name": "Orange Justice",
      "description": "blah blah blah",
      "link": "youtube url",
      "isComplete": true,
      
    }
  ```

