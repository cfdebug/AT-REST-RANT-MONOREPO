# Project REST-Rant
REST-Rant is an app where users can review restaurants. Add a new restaurant, or create a comment and rating on an existing one. Help others find the best place to enjoy a good meal!

## Demo
[Active demo can be seen here!](http://restrant-env.eba-nzyuh4nt.us-east-1.elasticbeanstalk.com/)

### Dependencies

|       Package       | Version  |
| ------------------- | -------- |
|        CORS         | v2.8.5   |
|     Body-Parser     | v1.19.0  |
|       Dotenv        | v10.0.0  |
|       Express       | v4.17.1  |
| Express-React-Views | v0.11.0  |
|   Method-Override   | v3.0.0   |
|       Nodemon       | v2.0.12  |
|         Pg          | v8.6.0   |
|      Pg-hstore      | v2.3.4   |
|        React        | v16.14.0 |
|      React-Dom      | v16.14.0 |
|      Sequelize      | v6.6.5   |
|    Sequelize-CLI    | v6.2.0   |

#### Deployed on AWS using Elastic BeanStalk


### Setup
First, you'll need a Postgres database to connect to. Follow instructions here to setup the database and save credentials for the next step.

Next create a `.env` file inside of `backend`. It will need to contain the following environment variables (change the values for the database to match what you defined in the previous step)
```
PORT=5000
DB_USERNAME=rest_rant_user
DB_PASSWORD=password
DB_DATABASE=rest_rant
```

Next `cd` into `backend` and run `npm install` to install dependencies for the API.

Next, `cd` into `frontend`, and run `npm install` to install dependencies for the React app.

Finally, in separate terminals, run `npm start` in each folder so that the API and React app are running at the same time.

### API (http://localhost:5000)
| Method | Path                                 | Purpose                                   |
| ------ | ------------------------------------ | ----------------------------------------- |
| GET    | /                                    | Home page                                 |
| GET    | /places                              | Places index page                         |
| POST   | /places                              | Create new place                          |
| GET    | /places/:placeId                     | Details about a particular place          |
| PUT    | /places/:placeId                     | Update a particular place                 |
| DELETE | /places/:placeId                     | Delete a particular place                 |
| POST   | /places/:placeId/comments            | Create a comment about a particular place |
| DELETE | /places/:placeId/comments/:commentId | Delete a comment about a particular place |


### App (http://localhost:3000)
| Path                  | Component                 | Purpose                                                                         |
| --------------------- | ------------------------- | ------------------------------------------------------------------------------- |
| /                     | `Home.js`                 | Home page                                                                       |
| /sign-up              | `users/SignUpForm.js`     | Form for creating a new user                                                    |
| /places               | `places/PlaceIndex.js`    | List of places                                                                  |
| /places/new           | `places/NewPlaceForm.js`  | Form for creating a new place                                                   |
| /places/:placeId      | `places/PlaceDetails.js`  | Details of a place, including it's comments, and a form to create a new comment |
| /places/:placeId/edit | `places/EditPlaceForm.js` | Form for editing a place                                                        |

## ChangeLog

- Completed Activity/Fixed Bug
- Create LICENSE
- adding login form to starter code
- added current user context
- Reverted oops
- added founded, seed data
- added founded, seed data
- in progress
- fixed layout issue
- updated ReadMe.md
- added nested author support
- bugfixes, added nested comment.author support
- in progress
- in progress
