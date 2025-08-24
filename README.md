Airbnb Clone Project

The Airbnb Clone Project is a real-world web application that simulates a booking platform like Airbnb. It focuses on full-stack development with Django, MySQL, and GraphQL, covering backend architecture, database design, API development, application security, and deployment. The project also emphasizes collaborative workflows with GitHub and CI/CD, helping learners gain hands-on experience in building scalable applications while practicing modern software engineering principles.


## Team Roles

A successful project like the Airbnb Clone requires collaboration across different specialized roles. Each role contributes unique expertise to ensure the system is scalable, secure, and user-friendly.

- **Backend Developer**  
  Focuses on building and maintaining the server-side logic, APIs, and integrations. They ensure that the application’s features work correctly, securely, and efficiently.

- **Frontend Developer**  
  Designs and implements the user interface, ensuring a smooth and responsive experience. They turn backend data into intuitive visuals for users.

- **Database Administrator (DBA)**  
  Manages the project’s database systems, ensuring data integrity, optimization, and security. The DBA also handles migrations, backups, and query performance tuning.

- **DevOps Engineer**  
  Handles CI/CD pipelines, deployment automation, and server management. They ensure the platform runs reliably in production and can scale when needed.

- **Quality Assurance (QA) Engineer**  
  Tests the system thoroughly to detect and report bugs. They verify that features meet requirements and maintain a high level of reliability.

- **Project Manager (PM)**  
  Oversees the project workflow, organizes tasks, and ensures deadlines are met. They coordinate communication across the team to keep progress on track.

- **UI/UX Designer**  
  Creates user-centered designs, wireframes, and prototypes. Their focus is on usability, accessibility, and ensuring the platform is visually appealing.

- **Security Engineer**  
  Implements and monitors security measures, including API protection, authentication, and data encryption, to keep the system safe from vulnerabilities.


  ## Technology Stack

The Airbnb Clone project leverages modern technologies to build a scalable and secure booking platform. Each tool plays a specific role in the system’s architecture:

- **Django**  
  A high-level Python web framework used to build the core application logic, handle user authentication, and provide a robust backend for APIs.

- **PostgreSQL**  
  A powerful relational database used to store and manage application data such as users, bookings, and property listings, with strong support for scalability and reliability.

- **GraphQL**  
  An API query language that allows clients to request exactly the data they need, improving efficiency compared to traditional REST APIs.

- **Git & GitHub**  
  Version control and collaboration tools that enable team members to track changes, manage branches, and work together seamlessly.

- **Docker**  
  Provides containerization to ensure the application runs consistently across different environments, simplifying deployment and scaling.

- **CI/CD Pipelines**  
  Automates testing, building, and deployment processes, ensuring that new updates are delivered quickly and reliably.

- **Nginx**  
  A web server and reverse proxy used to handle incoming requests, improve performance, and enhance security.

## Database Design

The database is designed to model the relationships between users, properties, and bookings in the Airbnb Clone system. Below are the key entities:

### Users
- **Fields**: `id`, `name`, `email`, `password`, `role` (guest/host/admin)  
- **Relationships**:  
  - A user can list multiple properties (if host).  
  - A user can make multiple bookings (if guest).  
  - A user can leave reviews for properties.

### Properties
- **Fields**: `id`, `title`, `description`, `location`, `price_per_night`, `host_id`  
- **Relationships**:  
  - A property belongs to one host (user).  
  - A property can have multiple bookings.  
  - A property can receive multiple reviews.

### Bookings
- **Fields**: `id`, `property_id`, `user_id`, `check_in_date`, `check_out_date`, `status`  
- **Relationships**:  
  - A booking is linked to one property.  
  - A booking is made by one user.  
  - A booking may be associated with a payment.

### Reviews
- **Fields**: `id`, `property_id`, `user_id`, `rating`, `comment`, `created_at`  
- **Relationships**:  
  - A review belongs to one property.  
  - A review is written by one user.

### Payments
- **Fields**: `id`, `booking_id`, `amount`, `payment_method`, `status`, `transaction_date`  
- **Relationships**:  
  - A payment is linked to one booking.  
  - Each booking can have one payment record.
