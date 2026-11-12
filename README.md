# Exp 12 - Simple Single Page Application (SPA) using React
## NAME: Hariharan S
## REG NO: 2305001009
## Aim
To develop a simple Single Page Application (SPA) using React JS with Home, About, and Contact pages and navigate between them using the useState hook.

## Objectives
- To understand the concept of Single Page Applications.
- To create reusable components in React.
- To use the useState hook for managing state.
- To implement navigation between different pages without reloading the browser.
- To apply CSS styling to the React application.

## Program

### 1. App.jsx

```jsx
import { useState } from "react";
import "./App.css";

function Home() {
  return (
    <div>
      <h2>Home Page</h2>
      <p>Welcome to Sukhmeet's React SPA!</p>
    </div>
  );
}

function About() {
  return (
    <div>
      <h2>About Page</h2>
      <p>This is a simple Single Page Application.</p>
    </div>
  );
}

function Contact() {
  return (
    <div>
      <h2>Contact Page</h2>
      <p>Email: sukhmeet@example.com</p>
    </div>
  );
}

function App() {
  const [page, setPage] = useState("home");

  return (
    <div className="app">
      <h1>Simple React SPA</h1>

      <nav>
        <button onClick={() => setPage("home")}>Home</button>
        <button onClick={() => setPage("about")}>About</button>
        <button onClick={() => setPage("contact")}>Contact</button>
      </nav>

      <hr />

      {page === "home" && <Home />}
      {page === "about" && <About />}
      {page === "contact" && <Contact />}
    </div>
  );
}

export default App;
```

### 2. App.css

```css
.app {
  text-align: center;
  padding: 30px;
}

nav {
  margin: 20px;
}

button {
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
}

button:hover {
  background-color: darkblue;
}
```

### 3. index.css

```css
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f2f2f2;
}

h1 {
  color: darkblue;
}

h2 {
  color: darkgreen;
}
```

### 4. main.jsx

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

## Output
<img width="1024" height="379" alt="image" src="https://github.com/user-attachments/assets/897df328-9f92-4082-9d1e-fdf6b4830900" />
<img width="1600" height="605" alt="WhatsApp Image 2026-11-05 at 10 32 01 AM" src="https://github.com/user-attachments/assets/23cf70e8-9f53-44f8-8a79-2ab3bed5899b" />
<img width="1024" height="380" alt="image" src="https://github.com/user-attachments/assets/b3832528-9713-4b38-a589-c5cd92db44e3" />

## Result
Thus, a simple Single Page Application was successfully developed using React JS with Home, About, and Contact pages. Navigation between the pages was implemented using the useState hook without reloading the browser.
