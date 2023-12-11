# CRUD Operations Decoded: Harnessing the Essence of Data Manipulation

Have you ever saved a contact on your phone, updated your profile information on a social media site, or just deleted some old files from your computer? Congratulations, you’ve already performed CRUD operations without even knowing it!

CRUD stands for Create, Read, Update, and Delete. These four actions are the core functions of persistent storage, which means when your information is stored for more than just your current session and won’t vanish into thin air once you’ve turned off your device.

## Breaking Down CRUD Operations

### Create ✨

Creating is just like making a new friend and saving their number in your contact list. In technical terms, ‘Create’ refers to adding new data to your database. For example, when you sign up for a new social media account, you’re creating a new record in that platform’s database.

Other examples:
-  Adding a new contact to your address book
-  Posting a new status update on social media

### Read 🔍

Reading might remind you of scrolling through your photos, reviewing past conversations with a friend, or skimming through your emails. It’s all about accessing data. In the data world, ‘Read’ operations involve fetching or viewing stored information from a database without making any changes to it.

Other examples:

- Looking up a recipe in a cookbook
- Checking your email inbox or social media feed for new messages

### Update 🔄

Updating your profile picture or contact information is a practical example of an ‘Update’ action. In the digital realm, this is about editing existing data. For example, when you update your delivery address on an online shopping site, you’re telling the database to replace the old information with the new one you’ve provided.

Other examples:

- Editing an existing document or presentation
- Updating your profile information on a website
### Delete 🗑️

Just cleared out your mailbox or emptied your recycle bin? That’s ‘Delete’. It’s about removing information that’s no longer needed. When you delete a file or an email, you’re instructing the system to remove that piece of data for good.

Other examples:

- Removing old files or unused apps from your computer to free up space
- Deleting spam or unwanted emails from your inbox

# Why are CRUD operations important?

CRUD operations form the foundation of most of the applications you use every day. Whether it’s shopping online, booking a flight, or simply browsing through a social media platform, all these actions require a way to create, read, update, or delete data.

The simplicity of CRUD operations makes them incredibly important for developers. They provide a clear and simple way to handle all the necessary interactions with the database.

In essence, learning about CRUD is like mastering the ABCs of interacting with the digital world’s data. It’s the starting point for entering the vast territory of programming and understanding how the digital products you love and use daily function at their core.


And that, my friends, is CRUD operations decoded. Simple, right? Just like creating a new playlist or organizing your desk – it’s all about managing information effectively. Now the next time you hit ‘save’, ‘edit’, or ‘delete’, remember, you’re doing a little bit of what developers do - manipulating the essence of data!

---

# The Role of CRUD in Programming
In programming, CRUD operations are like the four fundamental spells that every developer wields to bring their applications to life.

## What are CRUD operations used for in programming? 🤔
---
In programming, CRUD operations are like the four fundamental spells that every developer wields to bring their applications to life.

### `Create`
In programming, to ‘Create’ means to add new data. This could be a new user signing up for an app, creating a new blog post, or saving a new high score in a game.
```js
// Example in JavaScript using an array
let users = [];  
function createUser(username) {  
  users.push({ username: username });  
}
```
Other examples:
```js
let blogPosts = [];
function createPost(title, body) {
  blogPosts.push({ 
    title: title, 
    body: body 
  });
}
```
### `Read` 
‘Read’ operations are all about retrieving data. Think of it like asking a genie to fetch information from the vast sands of a digital desert.
```js
// Example in JavaScript
function getUser(username) {
  return users.find(user => user.username === username);
}
```
Other example:
```js
function getPost(title) {
  return blogPosts.find(post => post.title === title);
}
```
### `Update`
```js
// Example in JavaScript
function updateUser(oldUsername, newUsername) {
  let user = users.find(user => user.username === oldUsername);
  user.username = newUsername;
}
```
Other example:

```js
function updatePost(oldTitle, newTitle) {
  let post = blogPosts.find(post => post.title === oldTitle);
  post.title = newTitle; 
}
```

### `Delete` 

```js
// Example in JavaScript
function deleteUser(username) {
  users = users.filter(user => user.username !== username);
}
```
Other example:
```js
function deletePost(title) {
  blogPosts = blogPosts.filter(post => post.title !== title);
}

```
# Why is CRUD so crucial in programming? 💡

CRUD operations are omnipresent in programming. Just about any app you use—from social networks to banking apps—relies on these four actions to manage data. They allow users to have personal, dynamic experiences with technology. Without CRUD, your digital experiences would be static and unchanging—like a newspaper versus a live newsfeed.

There are a few reasons why CRUD is so fundamental to programming:

1. CRUD maps to real-world actions. Creating, reading, updating and deleting data correspond to basic interactions we have with the world every day. This makes CRUD intuitive for both developers and users.
2. CRUD enables rich, interactive applications. If an app couldn’t create, read, update or delete data, it would be lifeless. CRUD breathes life into apps by allowing users to save information, customize experiences, and accumulate data over time.
3. CRUD simplifies database interactions. Instead of having to write complex database queries for every little task, developers can use the simple CRUD operations. This allows them to focus on more challenging parts of building an application.
4. CRUD is standardized in REST. The REST architecture, which is used to build APIs and web services, maps HTTP request methods (POST, GET, PUT, DELETE) directly to CRUD operations. This standardization means developers can quickly understand how an API works.

Some examples of using CRUD in apps:


- **Create** : Sign up for a new account
- **Read** : Check your latest messages
- **Update** : Change your profile photo
- **Delete** : Remove an outdated post

---

# Let’s Build a Simple API with CRUD Operations

🌟 Ready to combine all the CRUD goodness with some real-life programming? We’re rolling up our sleeves and building a basic API, which is the backroom techie that handles requests from the app you see and love. Plus, we’ll make friends with a MySQL database to store all our precious data. Let’s break it down step-by-step, shall we?

## First Things First - What’s an API? 🤷‍♂️🤷‍♀️
---
API stands for Application Programming Interface. Think of it as a waiter in a restaurant – you tell them what you’d like (that’s your request), and they bring you the delicious food from the kitchen (that’s the response). Our API is going to take requests to create, read, update, and delete user data and then respond accordingly. Yum! ;-)

## Setting Up Our Kitchen – The MySQL Database

Before our waiter (API) can get to work, we need a kitchen – that’s our MySQL database. It stores all the data dishes we might want to serve up later.

## Cooking the Code – Node.js and Express

We’ll use Node.js to set up our API since it’s like having a versatile kitchen that can cook up anything we want quickly. Express is a framework that makes setting up Node.js apps a breeze – it’s like having all our pots and pans organized and ready to go.

# Ingredients (Dependencies) 

Make sure you’ve got Node.js installed, then we’ll add Express and the MySQL driver for Node.js, by running:


```bash
npm init -y
npm install express mysql body-parser
```

# Recipe for a Basic API
---
We’ll create a file called `server.js` and set up our Express server with mouth-watering CRUD routes.
```js
const express = require('express');
const mysql = require('mysql');

const app = express();
app.use(express.json());

// Connect salsa — config to connect our kitchen to the waiter
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'your_username',
  password: 'your_password',
  database: 'your_database_name'
});

connection.connect();

// CRUDdy routes cooking below

// Create (POST) - Taking the order
app.post('/users', (req, res) => {
  const { name, email } = req.body;
  connection.query('INSERT INTO users (name, email) VALUES (?, ?)',
                   [name, email], 
                   (error, results) => {
    if (error) throw error;
    res.status(201).send(`User added with ID: ${results.insertId}`);
  });
});

// Read (GET) - Serving up the dishes
app.get('/users', (req, res) => {
  connection.query('SELECT * FROM users', (error, results) => {
    if (error) throw error;
    res.status(200).json(results);
  });
});

// Update (PUT) - Spice up the order
app.put('/users/:id', (req, res) => {
  const { name, email } = req.body;
  const { id } = req.params;
  connection.query('UPDATE users SET name = ?, email = ? WHERE id = ?',
                   [name, email, id], 
                   (error) => {
    if (error) throw error;
    res.send('User updated!');
  });
});

// Delete (DELETE) - Cleaning up the plates
app.delete('/users/:id', (req, res) => {
  const { id } = req.params;
  connection.query('DELETE FROM users WHERE id = ?', [id], (error) => {
    if (error) throw error;
    res.send('User deleted.');
  });
});

// Time to open for business!
app.listen(3000, () => {
  console.log('API is listening on port 3000... Let the feast begin!');
});
```
Run this script with node server.js, and our API is alive!


# Interacting with Our API
Now we’ve got our waiter working and the kitchen is hot, our customers (clients making requests via HTTP) can:

- **POST to** `/users` to place a new user order (Create a user).
```json
POST /users 
{
  "name": "mahdi",
  "email": "mediishn@gmail.com" 
}
```
Response:
```json
201 Created
User added with ID: 5
```
- **GET from** `/users `  to see all the users we’ve created (Read users)
Request:
```json
GET /users
```
Response:
```json
200 OK
[
  { "id": 1, "name": "test", "email": "test@gmail.com" },
  { "id": 2, "name": "test2", "email": "jatest2ck@gmail.com" }  
]
```
- **PUT to** `/users/:id` with new info to update a user’s details (Update a user).
Request:
```json
PUT /users/2 
{
  "name": "test",
  "email": "test@gmail.com"
}
```
Response:
```json
200 OK
User updated!
```
- **DELETE at** `/users/:id`  to remove a user from the list (Delete a user).
Request:
```json
DELETE /users/1
```
Response:
```json
200 OK
User deleted.
```
---
# The Practical Magic Behind Everyday Tech ✨

In our digital day-to-day, CRUD operations work quietly to organize and manage the scattered puzzle pieces of our online life. Every status update, every photo saved, every playlist curated—they all come to life through the simple, yet powerful principles of Create, Read, Update, and Delete.

So, whether you’re a seasoned tech enthusiast or just dipping your toes into the digital stream, remember the simplicity and elegance of CRUD. They are the loyal stewards of our virtual world, diligently ensuring our digital interactions are seamless and intuitive.

As we close this chapter, don’t let the adventure end here. If you’re curious, inspired, or simply in the mood for a coding quest, why not come along for the ride?

Join the conversation and share your thoughts with me on Twitter: [`twitter`](https://twitter.com/m__mdy__m)

🤝 Want to build on your knowledge of CRUD? Your unique perspective would be a splendid addition to my learning journey. Let’s collaborate on my GitHub repository, and together we can learn, build, and maybe even teach along the way: [“Join Me in This Repository!”](https://github.com/m-mdy-m/nodejs-learning-journey)


[**<\mahdi>**](https://github.com/m-mdy-m)
