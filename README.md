# Project Overview – Drone Delights

**Drone Delights** is a responsive food delivery service built as a full-stack application. The project focuses on creating a simple but complete e-commerce experience with authentication, a custom backend, and a responsive interface that works on both desktop and mobile devices.

The goal was to build a realistic web application that demonstrates the full development process—from design and architecture to implementation and refinement.

## Design and Planning

The interface was initially designed in **Figma**, where the layouts for the desktop version were created. Designing the UI beforehand made it easier to translate the visual design into code, since measurements, spacing, and colors could be transferred directly into the implementation.

The UI was planned using a component-based approach from the beginning. Components were intentionally kept visually minimal and flexible, which made it easier to adapt the layout for mobile devices using media queries.

The project logo was also generated with the help of AI, which sped up the design phase and allowed more focus on the application itself.

## Implementation and Technology

The application was built incrementally, focusing first on functionality and logic before refining the visual design with CSS.

Early in development, **JSON Server** was used to simulate a database and quickly prototype data interactions. Later, it was replaced with a custom **Node.js backend** using **JWT authentication**, enabling a more realistic authentication flow with tokens and middleware.

To simplify data fetching and reduce repeated code, a custom React hook called **useFetch** was created. This helped centralize asynchronous requests and made the codebase easier to read and maintain.

Global state management was handled through several React contexts, including:

* **CartContext**
* **CategoryContext**
* **AuthContext**

Using contexts made it possible to share state and functions across the application without excessive prop passing, resulting in cleaner and more modular components.

A **ProtectedRoute** component was also implemented to restrict access to certain views. The user profile page (`/user`) requires authentication, while purchasing products is possible without being logged in.

### Technologies used

* **Figma** – UI design and layout planning
* **HTML / CSS** – structure and styling
* **Node.js** – backend development
* **JWT** – authentication system
* **JSON Server** – early data simulation
* **Masonry Layout** – flexible product card layout
* **FontAwesome** – icons
* **CSS variables** – centralized color and typography management

**Masonry Layout** was used to display product cards in a flexible grid, allowing cards to expand with additional information without breaking the layout.

Icons were implemented with **FontAwesome**, which made them easy to integrate and style directly in the markup.

Colors and typography were defined using CSS variables in `:root`, making it simple to maintain consistent styling and update themes across the entire application.

## Challenges and Solutions

### Backend Structure

One of the main challenges was structuring the backend logic. The initial implementation was inspired by earlier Node.js work but was adjusted significantly to better fit the needs of the project.

A notable improvement involved how favorites were handled. Instead of storing a boolean `isFavourite` value inside each product, favorites were stored as a list within the user's data. This made the system more flexible and easier to manage.

### Input Validation

A separate `validateInputs` utility function was created to handle form validation logic. This allowed real-time validation of fields such as usernames and passwords, providing visual feedback and clearer error messages for the user.

### Design Gaps

During development, it became clear how important complete planning is. One example was the order confirmation page, which had not been designed in advance. Designing directly in code proved to be slower compared to implementing a pre-planned layout.

### Managing a Growing Codebase

As the project expanded, maintaining a clear structure became more challenging. Consistent naming conventions turned out to be especially important, and several class names had to be refactored later in development.

The codebase was gradually improved by breaking larger components into smaller reusable ones—such as shared button components—which made the project easier to maintain and extend.

The folder structure eventually evolved into a hybrid between feature-based and type-based organization. This provided valuable experience in project structuring and highlighted the importance of choosing a clear and consistent architecture early in development.

## Future Improvements

There are several features that could expand the functionality of the application:

* Order history for users
* An admin panel for managing orders and users
* Improved filtering and search functionality
* Better feedback for actions such as adding items to the cart
* Small animations to create a more dynamic user experience

From a technical perspective, future versions of the project could also benefit from using a CSS framework such as **Tailwind** to improve styling structure and development speed.

## Summary

Drone Delights represents a complete full-stack project that combines frontend design, backend logic, authentication, and responsive UI development. It demonstrates how different parts of a modern web application interact and highlights the importance of planning, modular architecture, and iterative improvement.

The final result is a clean and simple web shop that provides a solid foundation for further development and additional features.
