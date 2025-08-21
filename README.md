# ERP_FE

## Requirements

- **Node.js:** Version 14.x or higher is recommended.
- **npm:** Comes with Node.js; ensure you have npm 6.x or later.
- **A modern web browser:** For testing and running the application.
- **Backend ERP API:** The application connects to a backend ERP system available at a configurable endpoint.

## Features

- **Production Batch Management:**  
  Supports operations such as fetching, updating, creating, and deleting production batches as part of the ERP workflow.

- **Recipe Integration:**  
  Fetch and update recipes linked to products, ensuring that production steps are defined and managed.

- **Packaging Operations:**  
  Handles packaging-related API calls including fetching packaging queues, starting packaging, updating packaging statuses, completing packaging, and viewing packaging statistics.

- **Inventory Management:**  
  Manages CRUD operations for inventory items and ingredients as implemented through the API service calls.

- **User Management:**  
  Features for creating, updating, and deleting users alongside role-based access, integrated via the admin API.

- **Retry Mechanism:**  
  Implements a retry mechanism (with exponential backoff) for API calls to ensure robustness against intermittent network issues.

## Introduction

ERP_FE is a front-end application built as part of an Enterprise Resource Planning (ERP) system. It is designed using React with functional components and hooks for state management. The application provides a modern interface for managing key operations in manufacturing and production environments including batch production, packaging, inventory control, and user operations. By seamlessly connecting to a backend ERP API, ERP_FE ensures that production workflows are efficient and data is synchronized between front-end interfaces and the backend services.

## Usage

- **Fetching Data:**  
  The application initializes by fetching production batches, packaging information, product lists, and inventory data. Data is retrieved through a set of well-defined API calls encapsulated in various API services (such as admin, factory, and packaging API services).

- **Managing Production Workflow:**  
  Users can select a production batch, view its recipe and associated production steps, and update the status as production proceeds. Functions like starting production, completing production steps, and finishing processing are available.

- **Packaging Dashboard:**  
  From the packaging dashboard, users can see available actions (like starting packaging, finishing packaging, and updating statuses) along with quick statistics about ready batches and ongoing packaging processes.

- **User Actions:**  
  Depending on user roles (such as admin or operator), actions for handling user creation, updating user information, and managing inventory are enabled. The interface uses a combination of React components and Material UI elements to provide an interactive and intuitive experience.

## Configuration

Several parameters can be configured to tailor the application to your environment:

- **API Endpoint:**  
  The base URL for API requests is defined in the environment variable `REACT_APP_API_URL` in the `.env` file. If not specified, the application defaults to a local development URL.

- **Timeout and Retry Settings:**  
  The factory API service includes settings for a request timeout (set to 10 seconds) and a maximum number of retries (set to 3) for API requests. These values can be adjusted directly in the service code if necessary.

- **Authorization Tokens:**  
  API service files retrieve authorization tokens from localStorage to authenticate API requests. Make sure that after login, the token is stored under the appropriate key (for example "token").

- **Styling and UI:**  
  The front-end makes extensive use of Material UI components. Customization of themes, components, and styling can be done by modifying the theme settings and component configurations in the application source files.

## Contributing

Contributions are welcome from the community. To get started:

1. **Fork the repository:**  
   Create your own branch from the main repository.

2. **Create a Feature Branch:**  
   Create a branch for your feature or bug fix. Use descriptive names (e.g., feature/packaging-enhancement, fix/inventory-bug).

3. **Develop and Test:**  
   Make modifications according to standard coding practices. Ensure your code is consistent with the existing codebase style. Write tests if applicable.

4. **Submit a Pull Request:**  
   Once your changes are ready, open a pull request. Please include detailed descriptions, screenshots if needed, and any information regarding the changes made.

5. **Follow Code Review Guidelines:**  
   Engage in constructive discussions during code reviews. All changes should pass continuous integration tests and meet the established quality standards.

Your contributions are greatly valued. Thank you for helping to improve ERP_FE!

---

This README provides a comprehensive guide to setup, use, and contribute to the ERP_FE project, which empowers production and packaging operations through a React-based front-end interface that integrates seamlessly with ERP backend services.