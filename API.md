# Moster API Documentation

## Authentication Endpoints
Authentication endpoints handle user registration, login, and account management. These endpoints are essential for securing user access and managing user sessions.

```markdown
Base URL: /api/auth

Public Endpoints:
POST /register                 - Register new user account
POST /login                    - Authenticate and get tokens
POST /refresh-token           - Refresh expired access token
GET  /confirm-email           - Verify email address
POST /reset-password          - Request password reset
POST /set-new-password        - Set new password after reset

Protected Endpoints:
POST /logout                  - Log out current user (requires auth)
```

## Content Management
The content management endpoints handle various types of content including AI-generated content, media files, and user activities. These endpoints are crucial for managing digital assets and user interactions within the platform.

```markdown
Base URL: /api/content
All endpoints require authentication

AI Content:
POST /ai-content              - Generate AI-powered content

Activities:
GET  /activities             - Fetch user activity history

Media Management:
GET    /medias              - Search/retrieve media files
POST   /medias              - Upload new media files
PUT    /media               - Update existing media
DELETE /medias              - Remove media files

Comments:
GET    /comments            - Retrieve comments
POST   /comment             - Add new comment
DELETE /comment             - Remove comment
POST   /comment/react       - React to comment
```

## Dashboard
Dashboard endpoints provide access to analytics, user settings, and workspace management. These endpoints are designed to support the main dashboard interface and user customization features.

```markdown
Base URL: /api/dashboard
All endpoints require authentication

Analytics:
GET /analytics              - Fetch dashboard metrics

User Management:
GET  /user-info            - Get user profile data
GET  /user-settings        - Retrieve user preferences
PUT  /user                 - Update user profile

Notifications:
GET  /notifications        - Get user notifications

Workspace Management:
GET    /workspaces         - List all workspaces (cached 7 days)
POST   /workspaces         - Create new workspace
DELETE /workspaces/{id}    - Remove workspace
```

## Posts
Post management endpoints handle the core content creation and scheduling functionality. These endpoints support the social media posting features of the platform, including reactions and media attachments.

```markdown
Base URL: /api/posts
All endpoints require authentication

Post Management:
GET    /                   - List all posts (cached)
GET    /post              - Get single post details
POST   /                   - Create new post
PUT    /                   - Update existing post
DELETE /                   - Remove posts

Post Interactions:
POST   /attach-media      - Add media to post
POST   /react             - React to post

Scheduling:
GET    /schedules         - View scheduled posts (cached)
```

## Workspace Management
Workspace endpoints handle team collaboration features, including member management and social media account integration. These endpoints are essential for multi-user environments and social media management.

```markdown
Base URL: /api/workspaces
All endpoints require authentication

Workspace Settings:
GET  /workspace           - Get workspace configuration
PUT  /workspace           - Update workspace settings

Member Management:
GET    /members           - List workspace members (cached 7 days)
POST   /members           - Add new members
PUT    /members           - Update member roles
DELETE /members           - Remove member

Social Media Integration:
GET    /social-media-accounts      - List connected accounts (cached 1 hour)
GET    /social-media-account       - Get single account details
POST   /social-media-accounts      - Connect new account
PUT    /social-media-accounts      - Update account settings
DELETE /social-media-accounts      - Remove connected account
```

## Technical Implementation Notes

### Authentication
```markdown
- Most endpoints require a valid authentication token
- Tokens should be included in the Authorization header
- Format: Bearer <token>
```

### Caching Strategy
```markdown
- Workspaces: 7-day cache
- Members: 7-day cache
- Social Media Accounts: 1-hour cache
- Posts and Schedules: Custom cache invalidation
```

### Error Handling
```markdown
- Standard HTTP status codes used
- 200: Success
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 500: Server Error
- Detailed error messages included in response body
```

### Response Format
```markdown
All endpoints return:
{
    "success": boolean,
    In case of error {        
    "Messages": [
            {
            "key": "*",
            "message": "Invalid credentials",
            "verbosity": 1
            }
        ]
    }
    Else
    {
        data properties..
    }
}
```
"*" value in key means that a business error occured, else it's a validation error and it will have the field name e.g. "email"

### Mocked Data
You can create a Mocked database via this endpoint:
GET    api/X/mock-data   

### Best Practices
```markdown
1. Always check response success property
2. Use the useApi hook
3. Cache responses where appropriate
4. Use skeleton loaders
5. Validate request data before sending
```
