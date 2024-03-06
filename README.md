# social-network-API
## Description

This project serves as the backbone for a social media platform's backend infrastructure. The API facilitates various user actions such as posting thoughts, reacting to friends' posts, and managing friend lists. Routing is handled through Express.js, while MongoDB serves as the database backend, complemented by Mongoose for Object Data Modeling. This project was completed with the help of Learning Assistant (provided insight and reminders of structural syntax), classmates/colleagues (who walked me through the process of setting up the project and the purpose of each component, as well as setting up the routes and how to test them in Insomnia), and of course online sources like W3 Schools, MDN.com, and StackOverflow. 

## Installation
To get started with this project, clone the repository and install the dependencies:
`git clone https://github.com/suzetsalinas/social-network-API.git `
` cd social-media-api `
` npm install `
After installation, start the server with:
` npm start ` 
The server will start running on localhost:3001.

## API Routes
### Users
GET /user: Get all users.
- eg. http://localhost:3001/user/
GET /user/:id: Get a single user by ID.
- eg. http://localhost:3001/user/65ab0754fd538e17b62f49f6
POST /user: Create a new user.
- eg. http://localhost:3001/user
- JSON: {
  "username": "testing",
  "email": "user@test.com"
}
PUT /user/:id: Update a user by ID.
- eg. http://localhost:3001/user/65ab2194ee5541a471227253
JSON: {
  "username": "testing1",
  "email": "user1@test.com"
}
DELETE /user/:id: Delete a user by ID.
- eg. http://localhost:3001/user/65ab01745cbb37d2fb2b98c1

### Thoughts
GET /thought: Get all thoughts.
- eg. http://localhost:3001/thought
GET /thought/:id: Get a single thought by ID.
- eg. http://localhost:3001/thought/65ab20f7ee5541a471227223
POST /thought: Create a new thought.
- eg. http://localhost:3001/thought/
- JSON: {
  "username": "test2",
  "thoughtText": "testing example"
}
PUT /thought/:id: Update a thought by ID.
- eg. http://localhost:3001/thought/65ab20f7ee5541a471227223
- JSON: {
	"thoughtText": "example test",
	"username": "test3"
}
DELETE /thought/:id: Delete a thought by ID.
- eg. http://localhost:3001/thought/65ab20f7ee5541a471227223

### Reactions
POST /thought/:thoughtId/reactions: Add a reaction to a thought.
- eg. http://localhost:3001/thought/65ab015e5cbb37d2fb2b98bb/reactions/
- JSON: {
	"reactionBody": "required",
	"username": "test4"
}
DELETE /thought/:thoughtId/reactions/:reactionId: Remove a reaction from a thought.
- eg. http://localhost:3001/thought/65ab015e5cbb37d2fb2b98bb/reactions/65ab2157ee5541a471227243

## Walkthrough Video
For a detailed walkthrough of the API, please visit this video link: https://app.screencastify.com/v3/watch/UtQZieJSGUPf1RFxLC7Y
