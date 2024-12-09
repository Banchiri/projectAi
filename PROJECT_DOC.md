Phase 4 Project Documentation
Project Overview
The goal of this project is to develop a full-stack application that leverages a Flask API backend and a React frontend to provide a cohesive and interactive user experience. The application will demonstrate your understanding of designing robust backends, building responsive frontends, and connecting them seamlessly.

The app will include at least three models, relationships, validation, authentication, and fully functional CRUD features.

Learning Goals
Backend Development:

Build a Flask API with models that represent a realistic data structure.
Include at least two one-to-many relationships.
Include one reciprocal many-to-many relationship with an additional user-submittable attribute.
Provide full CRUD actions for at least one resource and create/read actions for all resources.
Frontend Development:

Use React Router to create at least three client-side routes.
Implement a navigation bar (or similar UI component) for easy navigation.
Use Formik for form handling and validation.
Include at least one data type validation and one string/number format validation.
Full-Stack Integration:

Use fetch() to connect the backend and frontend for seamless data interaction.
UI/UX Design:

Create user-friendly forms with client-side validation.
Include meaningful feedback for user actions like submission success/errors.
Requirements Checklist
Backend Requirements (Flask API)
Models:

Minimum three models with realistic attributes.
At least two one-to-many relationships.
One reciprocal many-to-many relationship.
A many-to-many association model/table must include a user-submittable attribute beyond foreign keys.
CRUD Features:

Full CRUD for one resource (Create, Read, Update, Delete).
Create and Read actions for all other resources.
Data Relationships:

Models should have proper relationships with cascading actions (if required).
Relationships should reflect user stories effectively.
Validation:

Server-side validation for data type and format requirements.
Frontend Requirements (React)
Routes:

At least three distinct client-side routes using React Router.
Include protected routes for user-restricted areas (e.g., dashboard or profile).
UI Elements:

A navigation bar or equivalent UI for seamless navigation.
Clean and accessible interface design.
Forms and Validation:

All forms should use Formik with input validation.
Implement at least one:
Data type validation: Example, ensuring numeric input for quantity fields.
String/number format validation: Example, validating email or phone number formats.
Data Fetching:

Use fetch() to send and retrieve data between the backend and frontend.
User Stories
MVP (Minimum Viable Product):

As a user, I can register and log in to access personalized content.
As a user, I can create, view, and edit a primary resource.
As a user, I can navigate through different sections of the app using a navigation bar.
Stretch Goals:

As a user, I can filter or search data.
As a user, I can interact with other users or share content.
As a user, I can see visual feedback for actions (e.g., modals, toasts).
Technical Implementation
Backend Implementation
Models and Relationships:

Example:
User (One-to-Many with Post, Many-to-Many with Skill).
Post (Belongs to User).
Skill (Reciprocal many-to-many with User via a join table with attributes like level).
CRUD Actions:

Implement RESTful routes for resources, e.g.:
GET /users
POST /posts
PUT /skills/:id
DELETE /posts/:id
Validation:

Use Flask-WTF or Marshmallow for server-side validation.
Example:
Ensure email field follows proper format.
Ensure age is numeric.
Frontend Implementation
React Components:

Create reusable components:
NavBar: Includes links to all routes.
Form: Integrated with Formik for validation.
Card: Displays items like posts or skills.
Routes:

Example:
/login: Login page.
/dashboard: User dashboard (protected).
/resources: View/create resources.
Data Fetching:

Use fetch() to:
Retrieve user-specific data.
Post new entries to the backend.
Update or delete items in the backend.
Forms:

Use Formik and Yup:
Validate inputs (e.g., valid email, required fields).
Display error messages inline.
Execution Plan
Phase 1: Planning
Define models and their relationships.
Design wireframes for frontend routes.
Outline backend endpoints.
Phase 2: Backend Development
Set up Flask project structure.
Create and test models, migrations, and relationships.
Build and test RESTful API endpoints.
Phase 3: Frontend Development
Set up React project structure.
Build reusable components.
Create and style frontend routes.
Connect React to Flask API using fetch().
Phase 4: Testing and Deployment
Test backend and frontend independently.
Test integration using Postman and browser tools.
Deploy backend (e.g., Render) and frontend (e.g., Netlify).
Example Application
Scenario: A Blogging App
Models:

User:

Attributes: id, username, email, password.
Relationships: One-to-Many with Post.
Post:

Attributes: id, title, content, user_id.
Relationships: Belongs to User.
Tag:

Attributes: id, name.
Relationships: Many-to-Many with Post.
Join Table (for many-to-many):

post_tags:
Attributes: post_id, tag_id, user_rating (user-submittable).
CRUD Features:

Full CRUD for Post:
Users can create, view, edit, and delete posts.
Create/Read for Tag and User.
Deployment
Backend Deployment:

Deploy the Flask API using Render or AWS.
Use environment variables to secure sensitive data (e.g., database URI).
Frontend Deployment:
