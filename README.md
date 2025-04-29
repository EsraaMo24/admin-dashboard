## 💠 Admin Dashboard – Frontend (React)

An admin-only dashboard that allows store administrators to manage key settings and view general store statistics. The interface supports either mock data or real back-end integration.

---

### 📦 Requirements

- **Node.js** v14 or above  
- **React** (Vite or Create React App)  
- **React Router** for routing  
- **State Management:** using `useState` or `Context API`  
- **Optional:** Back-end API integration or local mock data

---

### 📁 Project Structure

```
admin-dashboard/
│
├── public/
├── src/
│   ├── components/       ← UI components (stats, toggles, etc.)
│   ├── pages/            ← AdminDashboard page
│   ├── routes/           ← Routing and access control
│   ├── context/          ← User context or mock user
│   ├── App.jsx
│   └── main.jsx
├── package.json
└── README.md
```

---

### 🚀 How to Run

```bash
# Install dependencies
npm install

# Run the project
npm run dev
```

---

### 🔒 Admin Access Control

- The app checks for `user.isAdmin` to allow access to `/admin` route.
- If no auth system exists, a mock user can be used:

```js
const currentUser = { name: "Admin", isAdmin: true };
```

- Non-admin users are either blocked or redirected away from `/admin`.

---

### 🧹 Key Features

- 🔐 **Admin-only access control**
- 📊 **View general store stats (e.g., total users, products...)**
- 🛠️ **Toggle maintenance mode**
- 📝 **(Optional) Edit store name and announcements**
- 🧪 **Basic access control testing**
- 🎨 **Clean and responsive UI design**

---

### ✅ Completed Tasks

- [x] Created `/admin` route and component
- [x] Checked `isAdmin` for protected access
- [x] Displayed placeholder statistics
- [x] Implemented toggle for maintenance mode
- [x] Restricted access for non-admin users
- [x] Applied minimal, user-friendly styling

---

### 🧪 Testing (Optional)

- Can use Jest or React Testing Library.
- Verify:
  - AdminDashboard only renders for `isAdmin: true`
  - Maintenance toggle is only visible to admins

---

### 📌 Additional Notes

- You can later connect to real APIs such as:
  - `GET /api/admin/settings`
  - `POST /api/admin/maintenance/toggle`

- The dashboard can also support displaying recent orders or users if backend data becomes available.

