### Questions

1. What is responsible for defining the routes of the `games` resource?
    A: the server.js file in combination with the create_router.js in the server folder.

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
    A: The client makes a request for a service, and a server performs that service

3. What are the the responsibilities of server.js?
    A: It interacts with the database and accesses the games collection, then creates routes for that resource. 


4. What are the responsibilities of the `gamesRouter`?
    A: gamesRoutes is what sets up the routes for the games resource by calling the createRouter function. 

5. What process does the the client (front-end) use to communicate with the server?
    A: the GamesService.js file handles the communication of the front-end and server, by fetching the API and updating it with POST or DELETE requests. 

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
    A: an init Object according to the MDN docs "an init object that allows you to control a number of different settings". On this case we used in order to make the correct request to the DB to add or remove game objects. 

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
    A: it uses the base 'http://localhost:5000/api/games/' for GET and POST
    and 'http://localhost:5000/api/games/:id' for DELETE. 

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
    A: for interaction between the server and the database. 

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
    A: to obtain the _id value of the objects and direct the routes to specific objects also allowing the Delete and Put actions on them. 

Add to your diagram the dataflow for removing a game.
