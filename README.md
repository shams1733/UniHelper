# UniHelper
You are helping me build a full-stack web application called "UniHelper" using:

- Frontend: Next.js (App Router) + TypeScript + TailwindCSS + React Query
- Backend: Next.js API Routes or separate Express.js service (we'll decide file by file)
- Database: MongoDB with Mongoose
- Auth: JWT Authentication (access + refresh token)
- UI Theme: Blue/White Academic Style (clean card UI)
- State Management: React Query
- Icons: Lucide-react

This is Phase-1 of UniHelper: **Room Finder System for University Students**

🎯 Main Goal:
Help students find verified hostel/room accommodations, and help hostel owners list rental spaces.

---

✅ **Core Functional Requirements – Phase 1**
1. **User Roles**
   - Student
   - Hostel Owner
   - Admin (later)
2. **Authentication**
   - Register/Login with Email & Password
   - JWT token stored in HttpOnly secure cookies
   - Password hashing
3. **User Profile**
   - Edit name, university ID, phone number, location
4. **Room Listings**
   - Owner creates room listings with:
     - Title
     - Description
     - Room Type (Shared/Single)
     - Price per month
     - City/location near campus
     - Images (store via Cloudinary)
     - Availability (Boolean)
5. **View Rooms** (Public + Auth user)
   - Search and filter rooms:
     - location
     - price range
     - type
6. **Room Details Page**
   - Display full room info + owner contact
7. **Request Booking**
   - Student sends request → Stored in DB
   - Owner sees pending requests and can accept/reject
8. **Owner Dashboard**
   - CRUD room listings
   - Manage booking requests
9. **Student Dashboard**
   - Track booking requests status (Pending/Accepted/Rejected)

---

⚙️ **Non-Functional Requirements**
- Responsive design for desktop/mobile
- Secure APIs (JWT & role-based access)
- Clean folder structure + reusable UI components
- Scalable schema design
- Success/error toast notifications
- Loading skeleton UI

---

🏗 **Project Architecture Requirements**
- Feature-based folder structure
- Use Next.js App Router with server components where appropriate
- Protect dashboard pages using middleware
- Use `.env` for all secrets (DB_URL, JWT_SECRET, CLOUDINARY_KEY, etc.)
- ESLint + Prettier + Husky formatting
- Git-friendly code → small modular components

---

🔐 Required API Endpoints – Phase 1
/auth/register
/auth/login
/auth/logout
/users/me
/rooms (POST owner)
/rooms (GET public)
/rooms/:id (GET public)
/rooms/:id (PATCH owner)
/rooms/:id (DELETE owner)
/bookings (POST student)
/bookings/owner (GET owner list)
/bookings/student (GET student list)
/bookings/:id (PATCH owner approve/reject)

---

🖥 UI Pages – Phase 1

Public Pages:
- Home (hero + search bar)
- Rooms listing (filter/search)
- Room details page
- Login / Register

Student Pages:
- Dashboard → My Requests
- Profile (edit)

Owner Pages:
- Dashboard → My Listings
- Add New Room Form
- Manage Requests

---

✅ What You Should Output First
1. Project folder setup
2. Tailwind + ESLint config
3. Base components + layout
4. Authentication pages + API
5. Role-based routing logic

After that, generate each feature incrementally with clean files and minimum hard-coding.

---

Before coding any large feature:
Ask me clarifying questions like:
“Do you want a modal or full page form?”
“Should the room images be carousel or grid?”
