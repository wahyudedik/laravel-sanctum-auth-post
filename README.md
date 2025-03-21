# Backend
- Laravel 12
- PHP 8.2
- MySQL 8.0
- Laravel Sanctum

## Aplikasi Fitur
- Login
- Logout
- Register
- Reset Password
- Profile
- CRUD POST

## Testing the API
You can use tools like Postman or Insomnia to test your API endpoints: 
Scrambel :http://127.0.0.1:8000/docs/api

### Authentication Endpoints

#### Register
- **URL**: POST /api/register
- **Body**: 
  - name
  - email 
  - password
  - password_confirmation

#### Login
- **URL**: POST /api/login
- **Body**:
  - email
  - password

#### Logout
- **URL**: POST /api/logout
- **Header**: Authorization: Bearer {token}

#### Forgot Password
- **URL**: POST /api/forgot-password
- **Body**:
  - email

#### Reset Password
- **URL**: POST /api/reset-password
- **Body**:
  - email
  - password
  - password_confirmation
  - token

#### Get Profile
- **URL**: GET /api/user
- **Header**: Authorization: Bearer {token}

#### Update Profile
- **URL**: PUT /api/profile
- **Header**: Authorization: Bearer {token}
- **Body**:
  - name
  - email

#### Update Password
- **URL**: PUT /api/password
- **Header**: Authorization: Bearer {token}
- **Body**:
  - current_password
  - password
  - password_confirmation

### Post Endpoints

#### Get All Posts
- **URL**: GET /api/posts
- **Header**: Authorization: Bearer {token}

#### Create Post
- **URL**: POST /api/posts
- **Header**: Authorization: Bearer {token}
- **Body**:
  - title
  - content
  - image (file)

#### Get Single Post
- **URL**: GET /api/posts/{id}
- **Header**: Authorization: Bearer {token}

#### Update Post
- **URL**: PUT /api/posts/{id}
- **Header**: Authorization: Bearer {token}
- **Body**:
  - title
  - content
  - image (file)

#### Delete Post
- **URL**: DELETE /api/posts/{id}
- **Header**: Authorization: Bearer {token}

#### Get User's Posts
- **URL**: GET /api/my-posts
- **Header**: Authorization: Bearer {token}