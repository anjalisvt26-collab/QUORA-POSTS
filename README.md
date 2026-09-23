Quora Posts – RESTful CRUD Web Application

A simple Quora-inspired web application built using Node.js, Express.js, EJS, HTML, and CSS.
This project demonstrates how a backend application can handle CRUD operations using RESTful routes and dynamic EJS templates.

The application allows users to create posts, view all posts, edit existing posts, and delete posts through a clean and simple interface.

📌 About The Project

The Quora Posts project is a backend-focused web application created to understand and practice RESTful routing and CRUD operations with Express.js.
Each post contains information such as:

* Unique Post ID
* Username
* Post Content

The application provides different routes to perform operations on these posts.
This project helped in understanding how the client, server, routes, templates, and HTTP methods work together in a web application.

✨ Features
* View Posts
Display all available posts.
Each post shows its username and content.
Posts are dynamically rendered using EJS.

#  Create Posts

Users can create a new post by providing a **username** and **post content** through a simple form.
When the user submits the form, the data is sent to the Express.js server using a **POST request**. The server receives the data and creates a new post object.
Each post is assigned a **unique ID using UUID (Universally Unique Identifier)**. This ID helps the application identify each post separately and perform operations such as editing or deleting a particular post.

For example:

Post ID: 7f3a21c9
Username: Anjali
Content: Learning Node.js and Express.js

#  View Posts

The application provides a posts page where users can view all the available posts.
Each post displays important information such as:

* Unique Post ID
* Username
* Post content
* Edit option
* Delete option

The posts are dynamically displayed using **EJS (Embedded JavaScript Templates)**. EJS allows the server-side data to be inserted dynamically into the HTML page.
For example, when the server has multiple posts, EJS loops through the posts and displays each post separately on the webpage.

#  Edit Posts

Users can update an existing post using its **unique post ID**.
When the user clicks the **Edit** button, the application uses the post ID to find the specific post. The existing username and content are then displayed inside an edit form.
After making changes, the user submits the form. The application sends the updated information to the Express.js server using a **PATCH request**.

The server finds the post using its ID and updates its content.

Example:

Before:
Username: Anjali
Content: Learning HTML

After:
Username: Anjali
Content: Learning HTML, CSS and JavaScript
This demonstrates how the **Update operation** works in a CRUD application.



# Delete Posts

Users can remove an existing post using the **Delete** button.
When the user clicks Delete, the application's delete route receives the **unique post ID** of that particular post.
The server uses this ID to identify the post and removes it from the posts collection.
After successful deletion, the user is redirected to the main posts page where the deleted post is no longer displayed.
This demonstrates the **Delete operation** of CRUD.



# Dynamic Routing

The application uses **Express.js dynamic routing** to work with individual posts.
Instead of creating a separate route for every post, a dynamic route can handle different post IDs.

For example:


/posts/:id
Here, `:id` is a **route parameter**.

If a user wants to edit a post with ID `12345`, the URL can be:
/posts/12345/edit


Express.js reads `12345` as the value of the `id` parameter.
The application can then use this ID to find the correct post from the posts collection.
For example:


let { id } = req.params;

This allows the application to access the ID from the URL and perform operations on the corresponding post.
Dynamic routing is mainly used in this project for:

* Identifying individual posts
* Editing specific posts
* Deleting specific posts
* Creating URLs based on post IDs



# RESTful CRUD Operations

This project demonstrates all four basic **CRUD operations**:
GET – Retrieve posts
POST – Create a new post
PATCH – Update an existing post
DELETE – Delete a post

Together, these operations form the core functionality of the Quora Posts application.
The project demonstrates how **HTML forms, Express.js routes, HTTP methods, EJS templates, UUID, and server-side data** work together to create a functional CRUD-based web application.
After deletion, the user is redirected back to the posts page.
🔗 RESTful Routing


