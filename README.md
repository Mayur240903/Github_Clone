# Git-Spliwise - A GitHub Replica

A full-stack MERN application that replicates GitHub's core functionality with custom version control implementation from scratch. This project demonstrates a complete Git-like version control system with repository management, user authentication, and collaboration features.

## Features

### Core Version Control
- **Custom Git Implementation**: Complete version control system built from scratch
- **Repository Management**: Create, clone, and manage repositories
- **Commit System**: Track changes with detailed commit messages
- **Branching & Merging**: Full branch support with merge capabilities
- **Push/Pull Operations**: Synchronize repositories with remote storage
- **Revert Functionality**: Rollback to previous commit states

### User Features
- **Authentication**: Secure user registration and login system
- **User Profiles**: Personalized dashboards and profile management
- **Repository Ownership**: Create and manage personal repositories
- **Collaboration**: Multi-user repository access and permissions

### Advanced Features
- **Real-time Collaboration**: Socket.io integration for live updates
- **Issue Tracking**: Create and manage repository issues
- **Cloud Storage**: AWS S3 integration for file storage
- **Modern UI**: GitHub-like interface using Primer design system

## Architecture

### Backend (Node.js + Express)
- **Framework**: Express.js with RESTful API design
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT-based authentication with bcrypt
- **Real-time**: Socket.io for live collaboration
- **Storage**: AWS SDK for S3 cloud storage
- **Version Control**: Custom Git implementation with file tracking

### Frontend (React + Vite)
- **Framework**: React 18 with modern hooks
- **Build Tool**: Vite for fast development and building
- **UI Library**: Primer React (GitHub's design system)
- **Routing**: React Router DOM for navigation
- **HTTP Client**: Axios for API communication
- **Testing**: Vitest with React Testing Library

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- AWS S3 bucket (for file storage)
- Git (for version control)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Github
   ```

2. **Install Backend Dependencies**
   ```bash
   cd backend-main
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../frontend-main
   npm install
   ```

4. **Environment Setup**
   
   Create a `.env` file in `backend-main`:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   S3_BUCKET=your_aws_s3_bucket_name
   AWS_ACCESS_KEY_ID=your_aws_access_key
   AWS_SECRET_ACCESS_KEY=your_aws_secret_key
   PORT=5000
   ```

5. **Start the Application**
   
   **Backend Server:**
   ```bash
   cd backend-main
   npm start start
   ```
   
   **Frontend Development Server:**
   ```bash
   cd frontend-main
   npm run dev
   ```



## Usage Examples

### Repository Operations

1. **Initialize a new repository:**
   ```bash
   node backend-main/index.js init
   ```

2. **Add files to staging:**
   ```bash
   node backend-main/index.js add <filename>
   ```

3. **Commit changes:**
   ```bash
   node backend-main/index.js commit "Your commit message"
   ```

4. **Push to remote:**
   ```bash
   node backend-main/index.js push
   ```

5. **Pull from remote:**
   ```bash
   node backend-main/index.js pull
   ```

6. **Revert changes:**
   ```bash
   node backend-main/index.js revert <commit-hash>
   ```

### Web Interface

1. **User Registration/Login**: Create an account or sign in
2. **Create Repository**: Initialize new repositories through the web UI
3. **Browse Repositories**: View and manage your repositories
4. **Collaborate**: Add collaborators and manage permissions
5. **Track Issues**: Create and manage repository issues
6. **View Commits**: Browse commit history and changes

## Technology Stack

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **Socket.io** - Real-time communication
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing
- **AWS SDK** - Cloud storage integration
- **Yargs** - Command line interface

### Frontend
- **React** - UI library
- **Vite** - Build tool and dev server
- **Primer React** - GitHub's design system
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Vitest** - Testing framework

## Testing

### Backend Testing
```bash
cd backend-main
npm test
```

### Frontend Testing
```bash
cd frontend-main
npm test
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile

### Repositories
- `POST /api/repos/create` - Create repository
- `GET /api/repos/:id` - Get repository details
- `PUT /api/repos/:id` - Update repository
- `DELETE /api/repos/:id` - Delete repository

### Issues
- `POST /api/issues/create` - Create issue
- `GET /api/issues/:repoId` - Get repository issues
- `PUT /api/issues/:id` - Update issue
- `DELETE /api/issues/:id` - Delete issue

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request






