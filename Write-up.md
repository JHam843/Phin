# WRITE_UP

## Description
This is a todo list of the application. We can add todo items to this application and manage the status of each todo list in the dashboard. You can add, update, delete, and complete the todo item in the todo list. This application is implemented by using React + Redux for front end, Node.js + Express.js for backend, and Firestore for the database.

## Run the application locally

- To install this project, `cd phin` `npm install` and `cd phin/view` and `npm install`
- To run this project, `npm run server` and `npm run client`

## Guide
As a consumer, you can add, update, delete, and complete the todo items.
And the application allow us to view the TODO items by their creation date, and show/hide the completed TODO items in the List Page. Also error handling for checking validate inputs in the adding or updating pages is implemeneted.

## Structure
1. Backend
  I implemeneted `MVC model` with Express in backend.
  - Express Server
    - Created a server running at the port 8000
    - By using express router, I implemented the APIs for providing `CRUD operations` for todo items.
    - Controller is responsible for handling all the routings and connecting to db
  - Firestore database
    - For using firestore database, I configured with my credential.
    - Models, this is in charge of accessing to the firestore db - so Creating, Fetching, Updating, and Deleting operations for db are implemented in this level.

2. Frontend
  - Pages

    There are some pages for todo application in front end. All the redux-state management are implemented in this page level.
    - Main
      This is just for brief introduction of the application.
    - List
      This is the main dashboard page for showing all the todos as a list.
    - Add
      This page is resposible for inputing all the details for one todo item and creating it.
    - Update
      This page is for updating the existing todo items with title and content.
  - Components

    Components are the pure element in the page.
    - TodoList
      This component is for showing all the todo items
    - TodoForm
      This component is structured as a template of a form for adding and updating one todo item.
  - Redux store

    For managing the global state of the application, I used redux-toolkit. Defined async actions for calling the API, and created reducers for managing the state.
  - Design
  
    I used Material UI and Flex Box for styling all of the components, and implementing the layout.

## Time I assigned
I mainly focused on implmenting the structure of this application.
 - Infrastructure (30mins)
    Structure the MVC model with Express server
 - Database & API (1hr)
    Firestore database config, connection and migrate with APIs with Express server
 - Front end Design (1.30mins)
    Build Components and Pages for TODO list
 - State Management in front end (1hr)
    Redux config, actions for API calls and integrate management with Pages in React.
