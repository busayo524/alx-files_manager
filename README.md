Files Manager
Project Description
Files Manager is a comprehensive backend application for managing files, users, and authentication. The project implements a robust API with multiple features including user registration, file upload, file management, and thumbnail generation.
Features
Core Functionality

User registration and authentication
File upload and management (supporting folders, files, and images)
File publishing and access controls
Image thumbnail generation
Redis and MongoDB integration

Endpoints
Authentication

POST /users: Create a new user
GET /connect: User login
GET /disconnect: User logout
GET /users/me: Get current user information

File Management

POST /files: Upload a new file or create a folder
GET /files: List files with pagination
GET /files/:id: Get specific file details
PUT /files/:id/publish: Make a file public
PUT /files/:id/unpublish: Make a file private
GET /files/:id/data: Retrieve file content

System

GET /status: Check system status
GET /stats: Get user and file counts

Technologies Used

Node.js
Express.js
Redis
MongoDB
Bull (for background job processing)
SHA1 (for password hashing)
mime-types
image-thumbnail

Environment Variables

PORT: Server port (default: 5000)
DB_HOST: MongoDB host (default: localhost)
DB_PORT: MongoDB port (default: 27017)
DB_DATABASE: MongoDB database name (default: files_manager)
FOLDER_PATH: Storage path for uploaded files (default: /tmp/files_manager)

Setup and Installation

Clone the repository
Install dependencies: npm install
Set up environment variables
Start the server: npm run start-server
Start the worker: npm run start-worker

Background Processing
The application uses Bull queues for:

Generating image thumbnails
Sending welcome emails (advanced feature)

Testing
Comprehensive test suites are available for:

Redis and MongoDB clients
All API endpoints
Authentication flows
File management operations

Advanced Features

Thumbnail generation for images
Background job processing
Welcoming email sending mechanism

Security Considerations

Passwords are hashed using SHA1
Authentication tokens are generated and managed securely
File access is controlled through public/private settings

Contribution
Please read the contribution guidelines before submitting pull requests.
