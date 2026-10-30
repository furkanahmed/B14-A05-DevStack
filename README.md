# 🧱 DevStack Builder — Interactive Tech Stack Explorer

DevStack Builder is an interactive, modern web application designed for developers to explore, compare, and assemble their ideal software development technology stack in real time.

---

## 🌐 Live URL & Repository

- **Live Application**: [https://devstack-live.netlify.app/](https://devstack-live.netlify.app/)
- **GitHub Repository**: [https://github.com/furkanahmed/B14-A05-DevStack](https://github.com/furkanahmed/B14-A05-DevStack)

---

## 📸 Preview Banner

<p align="center">
  <img src="src/assets/banner-stack.png" width="100%" alt="DevStack Builder Banner" />
</p>

---

## 📖 About The Project

DevStack Builder provides a streamlined visual interface where developers can browse popular frontend frameworks, backend runtimes, databases, styling libraries, and DevOps tools. Users can build their personalized stack side-by-side and manage their selections effortlessly with real-time feedback and state synchronization.

---

## 🛠️ Technologies Used

- **Frontend Library:** [React 18](https://react.dev/)
- **Build Tool:** [Vite](https://vitejs.dev/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) & [DaisyUI](https://daisyui.com/)
- **Icons:** [Lucide React](https://lucide.dev/) & DevIcon Vector SVGs
- **Toast Notifications:** [React-Toastify](https://fkhadra.github.io/react-toastify/)
- **Data Source:** RESTful Local JSON (`/data/technologies.json`)
- **Language:** JavaScript (ES6+)

---

## ✨ 5 Key Features

1. **Interactive Tech Stack Selection:** Browse 12+ curated technologies categorized into Frontend, Backend, Database, Language, Styling, and DevOps with real-time add/remove capabilities.
2. **Duplicate Prevention & Smart Toast Alerts:** Built-in validation prevents adding the same technology twice, displaying color-coded feedback (`React-Toastify`) for successful additions, duplicates, and removals.
3. **Real-time Live Stack Sidebar:** Dedicated responsive sidebar dynamically calculating selected stack counts, displaying selected technology cards, and enabling individual item deletion.
4. **One-Click Clear Stack (Remove All):** Quickly reset and empty the assembled technology stack with a single click, providing an instant state reset.
5. **Unified Modern Responsive Design:** Designed with a unified brand gradient system, custom CSS variables, and fluid responsive layouts for mobile, tablet, and desktop devices.

---

## 💡 Challenges & Solutions

- **Duplicate Stack Prevention:** Used `.some()` validation before state updates and integrated `react-toastify` alerts to stop duplicate entries smoothly.
- **SPA 404 on Refresh:** Configured `_redirects` (`/* /index.html 200`) and `netlify.toml` rewrite rules to ensure seamless routing on Netlify.

---

## 📦 Key Dependencies

- `react`: `^18.3.1`
- `react-dom`: `^18.3.1`
- `lucide-react`: `^0.460.0`
- `react-toastify`: `^10.0.5`
- `tailwindcss`: `^3.4.1`
- `daisyui`: `^4.12.10`
- `vite`: `^5.4.1`

---

## 🚀 Getting Started Locally

Follow these steps to clone and run the project locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/furkanahmed/B14-A05-DevStack.git
   cd B14-A05-DevStack
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```

4. **Open in browser:**
   Open [http://localhost:5173](http://localhost:5173) to view the application in action.

---

## 💡 React Conceptual Questions & Answers

### 1. What is JSX, and why is it used in React?
**Answer:** JSX (JavaScript XML) is a syntax extension for JavaScript that allows writing HTML-like structures directly inside JavaScript code. It is used in React because it makes building and reading UI components much simpler and intuitive compared to writing standard `React.createElement()` calls.

### 2. What is the difference between props and state?
**Answer:** 
- **Props (Properties):** Read-only data passed down from a parent component to a child component. The child component cannot modify props directly.
- **State:** Internal, mutable data managed within a component that determines its current behavior and UI. When state updates, React re-renders the component.

### 3. What does the `useState` hook do, and where did you use it in this project?
**Answer:** `useState` is a React hook that creates and updates reactive state variables within a functional component. In this project, `useState` was used in `App.jsx` to store the array of loaded technologies (`technologies`), the list of selected stack items (`stack`), and the fetch loading state (`loading`).

### 4. What does the `useEffect` hook do, and why did you need it to load the JSON data?
**Answer:** `useEffect` allows components to perform side effects, such as fetching data or setting timers, after rendering. We needed it to asynchronously fetch the technology list from `/data/technologies.json` once when the component initially mounts (`[]` dependency array).

### 5. Why does every item in a `.map()` list need a unique `key` prop?
**Answer:** React uses the unique `key` prop to identify which items in a list have changed, been added, or removed. It helps React efficiently update and re-render only the specific list item instead of re-rendering the entire list.

### 6. What is conditional rendering? Show one place you used it.
**Answer:** Conditional rendering means displaying different UI elements based on specific logical conditions (e.g., ternary operators `? :` or `&&`). In `YourStackSidebar.jsx`, we conditionally render either the empty stack message when `stack.length === 0` or the list of selected items when `stack.length > 0`.

### 7. How do you pass data from a parent component to a child component, and how does a child send something back to the parent?
**Answer:** Data is passed from parent to child via **props**. To send data back from a child to a parent, the parent passes a **callback function** as a prop to the child, which the child invokes with data when an event (like a button click) occurs.

---

## 👨‍💻 Author

**Furkan Ahmed** — [GitHub Profile](https://github.com/furkanahmed) • [Website](https://dremoy.com)
