# 🎓 Islamabad Universities Hub
### Complete Educational Portal – Full Stack Website

> Pakistan's most comprehensive university portal for Islamabad, covering all HEC-recognized institutions with admissions, fees, programs, scholarships, and an AI chatbot.

---

## 🌟 Features

- ✅ **10 Islamabad Universities** with complete real data
- ✅ **10-Tab University Detail Pages** (Overview, Admissions, Fees, Programs, Facilities, Rules, Faculty, Gallery, Student Portal, Careers)
- ✅ **University Comparison** (up to 3 side-by-side)
- ✅ **AI Chatbot** (UniBot – answers all queries)
- ✅ **Dark / Light Mode**
- ✅ **Admin Dashboard** (full CRUD)
- ✅ **Student Authentication** (Email + Google OAuth)
- ✅ **Scholarship Finder**
- ✅ **News & Announcements**
- ✅ **Admission Tracking** (Student Portal)
- ✅ **Fully Responsive** (Mobile + Desktop)

---

## 📁 Project Structure

```
islamabad-uni-hub/
├── client/          ← React Frontend (Vite)
│   ├── src/
│   │   ├── components/   (Navbar, Cards, ChatBot, etc.)
│   │   ├── pages/        (Home, Universities, Compare, etc.)
│   │   └── data/         (All university data)
│   └── package.json
│
└── server/          ← Node.js + Express Backend
    ├── controllers/
    ├── models/
    ├── routes/
    ├── middleware/
    ├── utils/
    └── server.js
```

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js v18+
- npm v9+
- MongoDB Atlas account (free)

---

### Step 1 – Download & Extract

Extract the ZIP file you downloaded. You will see:
```
islamabad-uni-hub/
├── client/
└── server/
```

---

### Step 2 – Frontend Setup

```bash
cd islamabad-uni-hub/client
npm install
npm run dev
```

✅ Frontend runs at: **http://localhost:3000**

That's it! The frontend works completely standalone with all university data built-in. No backend needed to view the website.

---

### Step 3 – Backend Setup (Optional – for full features)

```bash
cd islamabad-uni-hub/server
npm install
cp .env.example .env
```

Edit the `.env` file with your credentials:
- `MONGO_URI` – Get from [mongodb.com/atlas](https://mongodb.com/atlas) (free)
- `JWT_SECRET` – Any random 64+ character string
- `EMAIL_USER` / `EMAIL_PASS` – Gmail with App Password enabled

```bash
npm run dev
```

✅ Backend runs at: **http://localhost:5000**
✅ Health check: **http://localhost:5000/api/health**

---

### Step 4 – MongoDB Atlas Setup (Free)

1. Go to [mongodb.com/atlas](https://mongodb.com/atlas)
2. Create free account → Create free cluster
3. Database Access → Add user with password
4. Network Access → Allow from anywhere (0.0.0.0/0)
5. Connect → Drivers → Copy connection string
6. Paste in `.env` as `MONGO_URI`

---

## 📋 Available Pages

| Page | URL Path | Description |
|------|----------|-------------|
| Home | `/` | Hero, featured unis, news, scholarships, FAQ |
| Universities | `/universities` | All 10 universities with filters |
| University Detail | Click any card | 10 tabs with complete info |
| Compare | `/compare` | Side-by-side comparison |
| Scholarships | `/scholarships` | All scholarship programs |
| News | `/news` | Latest admission news |
| Contact | `/contact` | Contact form + FAQ |
| Auth | `/auth` | Login / Register |
| Admin | `/admin` | Admin dashboard |

---

## 🏛️ Universities Included

| # | University | Type | HEC |
|---|-----------|------|-----|
| 1 | Quaid-i-Azam University (QAU) | Public | W4 |
| 2 | COMSATS University Islamabad (CUI) | Public | W4 |
| 3 | National University of Sciences & Technology (NUST) | Public | W4 |
| 4 | Allama Iqbal Open University (AIOU) | Public | W4 |
| 5 | International Islamic University (IIUI) | Public | W4 |
| 6 | FAST National University (FAST-NUCES) | Private | W4 |
| 7 | Bahria University Islamabad (BU) | Public | W3 |
| 8 | Air University Islamabad (AU) | Public | W3 |
| 9 | Riphah International University | Private | W3 |
| 10 | University of Lahore – Islamabad Campus | Private | W3 |

---

## 🔌 API Endpoints

```
POST   /api/auth/register
POST   /api/auth/login
POST   /api/auth/google
GET    /api/auth/me
POST   /api/auth/forgot-password
POST   /api/auth/reset-password

GET    /api/universities
GET    /api/universities/search?q=nust
GET    /api/universities/compare?ids=id1,id2,id3
GET    /api/universities/:id
POST   /api/universities          (Admin only)
PUT    /api/universities/:id      (Admin only)
DELETE /api/universities/:id      (Admin only)

GET    /api/admissions/my
POST   /api/admissions
GET    /api/admissions/:id/track
PUT    /api/admissions/:id/status (Admin only)

GET    /api/scholarships
GET    /api/admin/stats           (Admin only)
GET    /api/admin/users           (Admin only)
POST   /api/admin/announcements   (Admin only)
```

---

## 🚢 Deployment

### Frontend → Vercel (Free)

```bash
cd client
npm run build
npx vercel --prod
```

Set environment variable in Vercel:
- `VITE_API_URL` = `https://your-backend.railway.app/api`

### Backend → Railway (Free)

1. Push `server/` folder to GitHub
2. Go to [railway.app](https://railway.app)
3. New Project → Deploy from GitHub
4. Add all `.env` variables in Railway settings
5. Done! Auto-deploys on every push.

---

## 🛡️ Security Features

- ✅ Helmet.js – Secure HTTP headers
- ✅ CORS – Domain-restricted
- ✅ Rate Limiting – 100 req/15min (10 for auth)
- ✅ JWT Authentication – 7-day expiry
- ✅ bcrypt – Password hashing (12 rounds)
- ✅ Input Validation – express-validator
- ✅ MongoDB Injection Prevention
- ✅ HTTPS in production

---

## 🤖 AI Chatbot

The built-in UniBot can answer questions about:
- University fees, rankings, programs
- Admission process and deadlines
- Scholarships and financial aid
- Entry tests (NET, QAU-NET, MDCAT, etc.)

Type "hi" to start a conversation!

---

## 👥 Team

Built by: **Sana Ullah & Team**
- Sana Ullah
- Hasna Ishtiaq
- Jaweria Shakoor
- Shahid Nawaz

---

## 📞 Support

- Email: info@islamabadunihub.pk
- Helpline: 0800-UNIHUB

---

*© 2025 Islamabad Universities Hub – Built with ❤️ for Pakistani Students*
