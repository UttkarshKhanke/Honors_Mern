# Simple Blog
## Requirement for a Simple Blog
The simple blog website should have two sections
1) Public area which is visible as home page of the site, this area will show content added by the authors.  There will be no login required for this content
2) Admin area which will be visited by navigating to Login link.  The admin area routes will be protected by user authentication
* The website should show recent blog post as main content
* The side panel on right should show the links to list of last 5 blog posts


```
Home
  Header
    SiteName (title)
    Login (link)
  Content
    Recent Post
  SideBar
    List of 5 recent posts
  Footer
    Copyright
Login
    Form
        Username (Label, textbox)
        Password (Label, textbox)
        Login (button)
Admin Section
  Home
  Users
  Create User
  Posts
  Create Post
Data Structure
User
  id
  name
  email
  password
  image
  biodata
  createdAt
  updatedAt
Post
  id
  title
  content
  image
  author (User)
  createdAt
  updatedAt
API Endpoints
GET /api/login
GET /api/users
POST /api/users
PUT /api/users/{userId}
DELETE /api/users/{userId}
/api/posts
GET /api/posts
GET /api/posts/user/{userId}
GET /api/posts/{postId}
POST /api/posts
PUT /api/posts/{postId}
DELETE /api/posts/{postId}
```

## Steps

Create frontend and backend folders
in frontend folder

```bash
npm install -g create-vite
npm create vite simple-blog -- --template react-swc
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

tailwind.config.js
```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
src/index.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

```bash
npm install -D react-router-dom
```

[React Tailwindcss NavBar Example](https://github.com/rrs301/react-tailwind-nav-bar)
[Spinner styling](https://www.material-tailwind.com/docs/html/spinner)
[Styling examples](https://v1.tailwindcss.com/components/buttons)