# xazyaeva_front
donation project

Frontend - Vue.js Application

A modern frontend for a charity platform, built on Vue.js 3 using Pinia for state management and Vue Router for navigation.

## 📋 Description

A web interface for the platform, providing users with an intuitive and convenient way to interact with the charity system.

## 🚀 Technologies

- **Framework**: Vue.js 3
- **State Management**: Pinia
- **Routing**: Vue Router 4
- **Build Tool**: Vite
- **HTTP Client**: Axios
- **Styling**: CSS3 (Custom)
- **Node Version**: ^20.19.0 || >=22.12.0

## 📦 Requirements

- Node.js 20.19.0 or higher (or 22.12.0+)
- npm or yarn
- Git

## 🔧 Installation and Run

### 1. Clone the repository

```bash
git clone https://github.com/Koreshzy0/xazyaeva_front
cd project-vue
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure the API

Make sure the backend server is running on `http://localhost:8080` or change the base URL in the `src/api/index.js` file.

### 4. Running in development mode

```bash
npm run dev
```

The application will be available at: `http://localhost:5173`

## 📁 Project Structure

```
project-vue/
├── public/ # Static files
├── src/
│ ├── api/ # API configuration
│ ├── components/ # Vue components
│ │ ├── EventCard.vue
│ │ └── ProjectCard.vue
│ ├── router/ # Vue Router configuration
│ ├── stores/ # Pinia stores
│ │ ├── useAuthStore.js
│ │ ├── useProjectStore.js
│ │ ├── useUserStore.js
│ │ ├── useCategoryStore.js
│ │ ├── useEventStore.js
│ │ └── useDonationStore.js
│ ├── views/ # Pages
│ │ ├── auth/ # Authorization
│ │ ├── projects/ # Projects
│ │ ├── events/ # Events
│ │ ├── categories/ # Categories
│ │ ├── users/ # Users
│ │ └── admin/ # Admin Panel
│ ├── App.vue # Main Component
│ └── main.js # Entry Point
├── package.json
└── vite.config.js
```

## 🎨 Main Pages

### Public Pages
- **Home** (`/`) - Main page with projects and statistics
- **Projects** (`/projects`) - List of all projects
- **Project Detail** (`/projects/:id`) - Detailed information about the project
- **Events** (`/events`) - List of volunteers Events
- **Event Detail** (`/events/:id`) - Event details
- **Categories** (`/categories`) - List of categories
- **About** (`/about`) - About us
- **Contacts** (`/contacts`) - Contacts

### Pages for authorized users
- **Login** (`/login`) - Login
- **Register** (`/register`) - Registration
- **Profile** (`/profile`) - User profile
- **Profile Edit** (`/profile/edit`) - Edit profile
- **User Profile** (`/users/:id`) - Another user's profile
- **Donate** (`/projects/:id/donate`) - Donation page

### Pages for NEEDS_HELP
- **Project Create** (`/projects/create`) - Create a project
- **Project Edit** (`/projects/:id/edit`) - Edit a project

### ADMIN Pages
- **Verification** (`/verification`) - Verify users and projects
- **Category Create** (`/categories/create`) - Create a category
- **Category Edit** (`/categories/:id/edit`) - Edit a category
- **Event Create** (`/events/create`) - Create an event
- **Event Edit** (`/events/:id/edit`) - Edit an event

## 🔐 Authentication

The application uses JWT tokens for authentication. The token is stored in cookies and automatically added to each request.

### User Roles

- **DONOR** - Donor (can make donations)
- **NEEDS_HELP** - Needy Person (can create projects after verification)
- **ADMIN** - Administrator (full access)

## 🎯 Main Features

### For all users
- View projects and events
- View categories
- View donation statistics
- Registration and login

### For donors (DONOR)
- Create donations
- View donation history

### For needy persons (NEEDS_HELP)
- Create projects (after verification)
- Edit your projects
- Upload documents for verification

### For administrators (ADMIN)
- Verify users and projects
- Manage categories (CRUD)
- Manage events (CRUD)
- Delete projects

## 🎨 UI/UX Features

- Responsive design for all devices
- Modern and clean interface
- Smooth animations and transitions
- Image carousel for projects
- Event cards with a beautiful design
- Intuitive navigation

## 📱 Responsiveness

The app is fully responsive and displays correctly on:
- Desktops (1920px+)
- Tablets (768px - 1024px)
- Mobile devices (< 768px)

## 🔧 Configuration

### API Base URL

Change the API base URL in `src/api/index.js`:

```javascript
const api = axios.create({
baseURL: 'http://localhost:8080/api/v1',
// ...
})
```

## 📦 Build and Deployment

### Production Build

```bash
npm run build
```

### Preview production build

```bash
npm run preview
```

## 🐛 Known issues

If you have any issues, please check:
1. Is the backend server running?
2. Is the API URL configured correctly?
3. Are all dependencies installed?

## 📄 License

This project is created for educational purposes.

## 📞 Contacts

For questions and suggestions, please create an issue in the repository.
