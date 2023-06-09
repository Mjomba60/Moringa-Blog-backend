# Phase 3 Project Guidelines

# Sinatra API

This is a Sinatra-based API that provides various endpoints for user and article management. It allows users to sign up, log in, create articles, add comments, and interact with likes.

## Prerequisites

- Ruby
- Sinatra
- ActiveRecord
- Bcrypt

## Getting Started

1. Clone the repository:

   ```bash
   git clone <repository-url>
  ````
2. Install dependencies:
  `bundle install`

3. start the application's development server
 `bundle exec rackup config.ru`

# Endpoints
## Home
`GET /`
Description: Returns a welcome message.
Response Body: `{ "message": "Good luck with your project!" }`

## Users
`POST /signup`

Description: Creates a new user account.
Request Body: `{ "first_name": "John", "last_name": "Doe", "user_name": "johndoe", "email": "john@example.com", "password": "password" }`

`POST /login`

Description: Authenticates the user and starts a session.
Request Body: `{ "user_name": "johndoe", "password": "password" }`

`GET /users`

Description: Retrieves all users.
`GET /users/:id`

Description: Retrieves a specific user by ID.
`DELETE /users/:id`

Description: Deletes a specific user by ID.

## Articles
`GET /articles`

Description: Retrieves all articles with associated comments and users.
`GET /articles/:id`

Description: Retrieves a specific article by ID with associated comments and users.
`POST /articles`

Description: Creates a new article.
Request Body: `{ "title": "Sample Article", "content": "This is a sample article." }`
`PUT /articles/:id`

Description: Updates a specific article by ID.
Request Body: `{ "title": "Updated Article", "content": "This is an updated article." }`
`GET /articles/:article_id/comments`

Description: Retrieves all comments for a specific article.
`POST /articles/:article_id/comments`

Description: Adds a new comment to a specific article.
Request Body: `{ "user_id": 1, "comments": "This is a comment." }`
`DELETE /articles/:article_id/comments/:comment_id`

Description: Deletes a specific comment from a specific article.
`GET /articles/:article_id/like`

Description: Retrieves all likes for a specific article.

## Likes
`POST /articles/:article_id/like`

Description: Adds a like to a specific article.
`POST /articles/:article_id/dislike`

Description: Adds a dislike to a specific article.
## Resources

- [create-react-app][]
- [dbdiagram.io][]
- [Postman][postman download]

[create-react-app]: https://create-react-app.dev/docs/getting-started
[create repo]: https://docs.github.com/en/get-started/quickstart/create-a-repo
[dbdiagram.io]: https://dbdiagram.io/
[postman download]: https://www.postman.com/downloads/
[network tab]: https://developer.chrome.com/docs/devtools/network/
