# Chinaar Kashmir Community Foundation (CKCF) Website

This is the official community membership and events management platform for the **Chinaar Kashmir Community Foundation** in Calgary.

The platform helps manage members (individuals and families), recurring payments, WhatsApp reminders, event listings, and admin tools for monitoring and outreach.

---

## 🌐 Live Site (Coming Soon)
**Domain:** [chinarkashmircommunityfoundation.ca](https://chinarkashmircommunityfoundation.ca)

---

## 📦 Features

### Member Management
- Register individuals or families (family head + dependents)
- Store gender, age, job/student status, over/under 18
- View family composition and size via queries

### Payments
- Monthly: $10 CAD, Yearly: $120 CAD, One-time joining fee: $25
- Stripe-powered recurring billing
- Family discount support (configurable)
- Payment status visible via green tick / red icon

### Communication
- Payment reminders via WhatsApp (Twilio API)
- No email communication required

### Member Portal
- Family login to manage profiles, view payment history
- Transfer dependents from student to job status
- View upcoming events

### Admin Tools
- Master accounts with access to all families
- Track who is or isn’t paying
- Send reminders
- View aggregate data (e.g., how many students, jobs, male/female)

---

## 🧱 Tech Stack

| Area        | Tech                            |
|-------------|---------------------------------|
| Frontend    | React / Next.js, Tailwind CSS   |
| Backend     | Node.js, Express.js             |
| Database    | PostgreSQL with Prisma ORM      |
| Auth        | JWT (or Clerk/Auth0)            |
| Payments    | Stripe                          |
| Messaging   | Twilio WhatsApp API             |
| Deployment  | Vercel (frontend), Railway/Render (backend) |

---

## 🛠️ Local Setup

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/chinaar-community-portal.git

# 2. Set up the backend
cd server
npm install

# 3. Set up the frontend
cd ../client
npm install

# 4. Create `.env` files
# Backend .env:
DATABASE_URL=your_postgres_url
JWT_SECRET=your_secret
STRIPE_SECRET_KEY=your_stripe_key
TWILIO_AUTH_TOKEN=your_twilio_token
...

# Frontend .env:
NEXT_PUBLIC_API_URL=http://localhost:4000

# 5. Run both servers (separately or use a dev proxy)
