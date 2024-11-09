# Mosyter Documentation

> <img src="./ui/wireframes/threat.png" alt="Important Note Icon" width="64" height="64" /> 

> **Important Note:**  
> The wireframes provided are intended solely to describe the **functionality** and **behavior** of the application, not its final design or visual style. They outline layout, content organization, and interaction flow but do not represent the color schemes, typography, or styling choices that will be applied in the final UI.

**Platform Overview**
Mosyter helps teams manage and schedule their social media content across multiple platforms using AI assistance, collaborative workspaces, and comprehensive content management tools.

## 1. Login & Authentication

### Login Page
The user lands on a clean login page where they can input credentials or reset password. After successful login, they enter the main dashboard with a top navigation bar showing the logo, main tabs (Workspaces/Posts/Media), notifications bell, and profile section.
Users see:
- Large card with:
  * Mosyter logo
  * Email field
  * Password field
  * "Remember me" checkbox
  * Login button
  * "Sign Up" / "Forgot?" links

Users can:
- Input credentials
- Save login information
- Reset password
- Create new account

---

## 2. Main Dashboard

### Navigation Bar
A fixed navigation bar at the top of the app shows the Mosyter logo followed by a Workspaces dropdown, and two tabs: Posts and Media Studio. The Workspaces dropdown allows quick navigation between workspaces and includes a "Create New" option at the bottom, using the html dropdown component of the styleguide. The active tab is visually highlighted. On the right side,a button Upgrade plan is shown followed by a notification bell that shows unread count in a bubble, followed by the user's profile picture which reveals a dropdown menu when clicked (containing Profile Settings, Help Center, and Logout). The bar remains consistent and accessible throughout the app's navigation. 

![alt text](/ui/wireframes/navbar.png)
Users see:
- Fixed top bar containing:
  * Mosyter logo (left)
  * Main tabs: Workspaces/Posts/Media
  * Notification bell (right)
  * Profile picture/menu (right)

Users can:
- Switch main sections
- View/clear notifications
- Access profile settings
- Log out

### Home Dashboard
The user sees a grid of workspace cards, each showing a logo, name, and member count. A create workspace button appears at the top. When clicking a workspace card, they enter the workspace dashboard. They can also delete workspaces or access workspace settings through card actions.
Users see:
- Grid layout of workspace cards:
  * Workspace logo/image
  * Workspace name
  * Member count
  * Posts count
  * Recent activity

Users can:
- Create workspace
- Enter workspace
- Delete workspace (with confirmation)

### Posts Tab
The user sees a header with view toggle (Kanban/List) and filter button. In Kanban view, they see three columns (Draft/Ready/Template) with a create button at the top of Draft column. In List view, they see an infinite scrolling list. When clicking the filter button, a collapsible left panel appears with search and filter options.

![alt text](/ui/wireframes/posts.png)

Users see:
- Header controls:
  * View toggle (Kanban/List)
  * Filter button
- Content area based on selected view:
  * Kanban: Three columns (Draft/Ready/Template)
  * List: Scrollable post list with filters

Users can:
- Switch views
- Filter posts
- Create new posts
- Drag posts between columns (in Kanban)
- Click to open post details

### Media Studio Tab
The user sees a top search bar with type filters (All/Images/Videos) and a two-panel layout. The left panel shows Private and Stock media lists with upload/import buttons. The main workspace shows either selected media preview with editing options or an import placeholder. When clicking import, a panel appears with stock media search.

![alt text](/ui/wireframes/medias.png)

Users see:
- Top search bar with type filters (All/Images/Videos)
- Left panel showing:
  * Private media section
  * Stock media section
- Main workspace showing:
  * Selected media preview/editor
  * Or import placeholder

Users can:
- Search all media
- Filter by type
- Upload/import media
- Edit media properties
- Delete media

---

## 3. Workspace Dashboard
The user sees a top bar with three sections: team members list (left), social media accounts (middle), and create post button (right). Below, they see a calendar view with scheduled posts. On the left, a collapsible panel shows Posts and Comments tabs. The calendar header contains view controls and navigation tools.

![alt text](/ui/wireframes/workspaceDashboard.png)

### Top Bar
Users see:
- Left: Horizontal team members list + add button
- Middle: Social media account toggles
- Right: Create post button

Users can:
- Add/manage team members
- Toggle social accounts
- Start post creation

### Calendar View
Users see:
- Calendar header with:
  * Left: View switch (Calendar/List)
  * Middle: Date navigation
  * Right: Week/Month toggle
- Main calendar grid
- Left action panel (collapsible) with:
  * Two tabs: "Posts" and "Comments"
  * Filter controls
  * Content list

Users can:
- Switch calendar views
- Navigate dates
- Toggle action panel
- Filter content
- View/add comments

---

## 4. Modal Systems

### Workspace Settings Modal
When clicking workspace settings, the user sees a modal with four centered tabs:
- Workspace: Basic info form (title, timezone, status, image)
- Timetable: Weekly posting schedule grid
- Notifications: Toggle list for notification types
- Tags: Colored tag management list

![alt text](/ui/wireframes/woekspaceSettings.png)

Users see:
- Four tabs:
  * Workspace (name, timezone, status)
  * Timetable (preferred posting times)
  * Notifications (toggle settings)
  * Tags (colored tag management)

Users can:
- Edit workspace details
- Set posting schedule
- Manage notifications
- Create/edit tags

### Members Management Modal
When managing team members, the user sees a modal with four tabs:

- Invite: Email form with role selection
- Members: List of members with role badges and actions
- Permissions: Matrix table for access control
- Notifications: Grid for notification preferences

![alt text](/ui/wireframes/membersSettings.png)
![alt text](/ui/wireframes/membersPermissions.png)

Users see:
- Four tabs:
  * Invite (email form + role selection)
  * Members (list with roles)
  * Permissions (access matrix)
  * Notifications (per-member settings)

Users can:
- Invite members
- Manage roles
- Set permissions
- Configure notifications

### Social Media Account Settings Modal
When configuring a social account, the user sees a profile-style modal with:

- Header showing platform info and reconnect button
- Two tabs: Content Themes (tone sliders) and Notifications
- Delete option with warning message

![alt text](/ui/wireframes/socialMediaSettings.png)

Users see:
- Account header with reconnect option
- Two tabs:
  * Content Themes (tone sliders)
  * Notifications (toggle settings)
- Delete account button

Users can:
- Adjust content themes
- Manage notifications
- Reconnect account
- Delete account

### Create Post Modal
When clicking Create Post button, the user sees a modal with social media accounts at the top as toggleable pills to select target platforms, with a plus button at the end to add more accounts. Below, there's a content area with text editor and media preview zone. A toolbar under the editor contains: media upload button (opens right side panel), GIF selection, emoji picker, location picker, and audience settings. The AI tool button in the toolbar opens a dropdown with: Generate, Complete, Rewrite, and Ideas. At the bottom of the modal, the user sees time selection (opens dropdown with workspace's preferred timetable) and action buttons (Save Draft, Schedule). When clicking media upload, a right panel slides in showing the media library grid with upload button and search functionality. The user can either upload from computer, select from existing media, or search GIFs.

![alt text](/ui/wireframes/postCreate.png)

Users see:
- Social media account toggles
- Content editor with:
  * Text area
  * Media attachment area
  * Tool bar (media, GIF, emoji, location)
  * AI assistant dropdown
- Side panel for media selection
- Bottom bar with:
  * Timetable selection
  * Draft/Schedule buttons

Users can:
- Select target platforms
- Write/edit content
- Add media
- Use AI assistance
- Set location/audience
- Schedule post
- Save as draft

### Post Settings Modal
### Post Settings Modal
When clicking a post, a full-screen modal appears with a mini left sidebar containing a Ready/Draft toggle switch at top, followed by a vertical list of targeted social media platform icons (each showing remove button on hover), a plus button at the end for adding platforms, and the author's avatar at the bottom. The main header shows colored tag pills with a dropdown to add/edit tags on the left, and on the right: an AI tool button (dropdown with Generate, Complete, Rewrite), a three-dot menu (containing Audience Settings, Copy Post, Set as Template, Detach, Delete), and a close button. The main content area has navigation arrows (left) to switch between platform previews and a mobile/web toggle (right), followed by the content editor and preview area (if Mobile or Web not checked then its the edit mode else its a preview mode). A right sidebar shows two tabs: Comments and Activity, displaying the conversation thread or change history respectively. When clicking a platform icon in the mini sidebar, the content area updates to show that platform's specific preview.
keep the same features of the post create modal in here.

![alt text](/ui/wireframes/postSettings.png)

Users see:
- Left mini sidebar with:
  * Ready/Draft status toggle
  * Vertical list of targeted social media accounts
  * Add platform button
  * Author avatar
- Header panel with:
  * Left: Colored tag pills and dropdown to add/create tags
  * Right: AI button, three-dot menu for these actions (Audience Settings, Copy Post, Set as Template, Detach, Delete), close button
- Content editor with:
  * Platform navigation (up/down arrows)
  * Mobile/Web preview toggle
  * Text area and media preview
  * Character count and constraints
- Right sidebar with:
  * Comments/Activity tabs
  * Threaded conversations
  * Change history
- Bottom actions:
  * AI suggestions
  * Media options
  * Schedule controls
  * Save/Publish buttons

Users can:
- Toggle post status
- Add/Remove target platforms
- Manage tags and settings
- Navigate between platforms
- Edit content and media
- Switch preview modes
- View/Add comments
- Track post history
- Use AI assistance
- Set scheduling
- Save draft or publish
- Copy/Delete/Template post
- Close modal

---

## 5. Global Features
The user has access to an AI assistant chat bubble in the bottom right corner at all times. When clicked, it opens a chat interface where they can request content generation, image searches, or writing assistance.
The user sees notifications in the top bar for all workspace and post activities. When clicking a notification, they are taken to the relevant section or item.
### AI Assistant
Users see:
- Fixed chat button (bottom-right)
- Chat overlay when opened:
  * Suggestion chips
  * Input field
  * Message history

Users can:
- Get content suggestions
- Search media
- Get writing assistance
- Execute quick actions

### Notifications System
Users see:
- Counter on bell icon
- Dropdown list showing:
  * Post updates
  * Comments
  * Team changes
  * System notifications

Users can:
- View notifications
- Mark as read
- Take quick actions
- Set preferences

---

## 6. Navigation Patterns

### Global Navigation:
- Top bar always visible
- RTL supported
- Dark mode supported (monochrome mode is a nice to have)
- Use rich html components (dropdown, toasts..)

### Modal Navigation:
- ESC to close
- Click outside to dismiss
- Consistent position of action buttons
- Clear header with close button

### Workspace Navigation:
- Quick switch between views
- Persistent team/social account bar
- Collapsible panels
- Save state between sessions

````mermaid

graph TB
    %% Main Entry
    Entry[Login Page] --> Dashboard[Main Dashboard]
    
    %% Main Navigation Level
    Dashboard --> |"Top Nav"| Nav{Navigation Bar}
    Nav --> WorkspacesTab[Workspaces Tab]
    Nav --> PostsTab[Posts Tab]
    Nav --> MediaTab[Media Studio Tab]
    Nav --> NotifBell[Notifications]
    Nav --> ProfileMenu[Profile Menu]
    
    %% Workspaces Flow
    WorkspacesTab --> WorkspaceGrid[Workspace Cards Grid]
    WorkspaceGrid --> WorkspaceDash[Workspace Dashboard]
    WorkspaceGrid --> WSSettings[Workspace Settings Modal]
    
    %% Workspace Dashboard Components
    WorkspaceDash --> TopBar[Top Bar]
    TopBar --> TeamList[Team Members List]
    TopBar --> SocialAccounts[Social Media Accounts]
    TopBar --> CreatePost[Create Post Button]
    
    WorkspaceDash --> CalendarView[Calendar View]
    CalendarView --> ViewControls[View Controls]
    ViewControls --> WeekMonth[Week/Month Toggle]
    ViewControls --> DateNav[Date Navigation]
    
    WorkspaceDash --> ActionPanel[Left Action Panel]
    ActionPanel --> PostsView[Posts Tab]
    ActionPanel --> CommentsView[Comments Tab]
    
    %% Posts Management
    PostsTab --> ViewToggle{View Type}
    ViewToggle --> KanbanView[Kanban View]
    ViewToggle --> ListView[List View]
    
    KanbanView --> |"Columns"| Columns{Kanban Columns}
    Columns --> Draft[Draft]
    Columns --> Ready[Ready]
    Columns --> Template[Template]
    
    %% Media Studio
    MediaTab --> MediaSearch[Search Bar]
    MediaTab --> MediaList[Media List]
    MediaList --> PrivateMedia[Private Media]
    MediaList --> StockMedia[Stock Media]
    MediaTab --> MediaPreview[Preview/Editor]
    
    %% Modals
    subgraph Modals [Modal System]
        WSSettings --> |"Tabs"| WSSettingsTabs{Workspace Settings}
        WSSettingsTabs --> WS_General[General]
        WSSettingsTabs --> WS_Timetable[Timetable]
        WSSettingsTabs --> WS_Notif[Notifications]
        WSSettingsTabs --> WS_Tags[Tags]
        
        MembersModal[Members Modal] --> |"Tabs"| MembersTabs{Members Management}
        MembersTabs --> M_Invite[Invite]
        MembersTabs --> M_List[Members List]
        MembersTabs --> M_Perms[Permissions]
        MembersTabs --> M_Notif[Notifications]
        
        SocialModal[Social Account Modal] --> |"Tabs"| SocialTabs{Social Settings}
        SocialTabs --> S_Themes[Content Themes]
        SocialTabs --> S_Notif[Notifications]
        
        PostModal[Post Modal] --> PostContent[Content Editor]
        PostModal --> PostSidebar[Right Sidebar]
        PostSidebar --> P_Comments[Comments]
        PostSidebar --> P_Activity[Activity]
    end
    
    %% Global Features
    subgraph Global [Global Features]
        AI[AI Assistant]
        Notifications[Notifications System]
        Search[Global Search]
    end
    
    %% Styling
    classDef page fill:#f9f9f9,stroke:#333,stroke-width:2px
    classDef modal fill:#e6e6e6,stroke:#666
    classDef nav fill:#d4e6f1,stroke:#2874a6
    class Entry,Dashboard,WorkspaceDash page
    class WSSettings,MembersModal,SocialModal,PostModal modal
    class Nav,TopBar,ViewControls nav
    
    %% Links
    TeamList --> MembersModal
    SocialAccounts --> SocialModal
    CreatePost --> PostModal
    AI --> Dashboard
    AI --> WorkspaceDash
    AI --> PostModal
