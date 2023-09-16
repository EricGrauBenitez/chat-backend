Hello World! I'm Eric Grau, and this is my final project for the Full Stack Web Development course at IT Codespace school. I've decided to create a chat application with ChatGPT's AI, as its functionality has exploded during the course, and the world is changing thanks to it. Because of this, it's essential to know how to apply it.

GET START

Requirements
Make sure to have a text and code editing tool like Visual Studio Code installed and set up NPM.

Install
Node.js

To download Node.js from the BASH terminal:
sudo npm install -g n
sudo n latest

Check the Node.js version with:
node -v

Clone the repository
In your directory:
npm install
BACK-END EXPLANATION
I chose Node.js and MongoDB because they share the same programming language and are very versatile. Moreover, the database system was not very complex and can be easily managed with these technologies.

User
User example:
{
"name": "User's Name",
"lastName": "User's Last Name",
"city": "City (optional)",
"country": "Country (optional)",
"email": "email@example.com",
"password": "secure_password",
"chats": [
{
"_id": "ID_OF_CHAT_1",
"conversation": [],
"title": "Chat Title 1",
"createdAt": 1631295667000
}
]
}


| Table with user endpoints: |
| URL                                      | TYPE  | DESCRIPTION                               |
|------------------------------------------|-------|-------------------------------------------|
| http://localhost:8000/users/:id          | GET   | get user data by id                       |
| http://localhost:8000/users/register     | POST  | create of an user                         |
| http://localhost:8000/users/email        | POST  | change with the email (forgot the password)|
| http://localhost:8000/users/:id          | PUT   | update an user by id                      |
| http://localhost:8000/users/:id          | DELETE| delete an user by id                      |
| http://localhost:8000/login              | POST  | create a token for the auth               |

| Table with chat-related endpoints: |
| URL                                      | TYPE  | DESCRIPTION                               |
|------------------------------------------|-------|-------------------------------------------|
| http://localhost:8000/chat/:userId/:chatId | GET  | get user chat by id                       |
| http://localhost:8000/chat/:userId/      | POST  | create a chat                              |
| http://localhost:8000/chat/conversation/:userId/:chatId | PUT | clean a conversation                |
| http://localhost:8000/chat/:userId/:chatId | DELETE| delete a chat by id                      |


In your .env file, add this field for login:
JWT_SECRET="Insert_your_secret_key_here"
