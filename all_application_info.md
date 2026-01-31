
# Rankbook Platform – MVP

Rankbook is an EdTech training and internship platform designed to:
1. Capture high-quality leads  
2. Convert leads into paying students  
3. Deliver education reliably  
4. Track outcomes and revenue accurately  

The platform supports both:
- **Cohort-Based Batches**
- **Self-Paced Courses**
- **Mass Public Tests** (Scholarship, Competitive, Entrance Exams)

AI features are intentionally deferred to Phase-2.  
The MVP focuses on **execution discipline and business viability**.

---

## 🧠 Product Philosophy

Rankbook is not “just” an LMS.  
It is a **business operating system for an EdTech company**.

The product is built around four hardened systems:

| System | Purpose |
|------|-------|
| Public Website | Lead generation & purchase engine |
| CRM Dashboard | Sales, finance, and communication control center |
| LMS User App | Learning delivery & testing |
| LMS Admin Dashboard | Academic operations & content management |

Each system owns its domain.  
No feature overlaps.



## 🏗️ System Architecture

```

Public Website ←→  Payment Gateway
↓
CRM Dashboard  ←→  Payment Gateway
↓
LMS User App
↑
LMS Admin Dashboard

```


## 🚀 MVP Scope

### 1. Public Website – *Lead & Purchase Engine*

**Purpose:**  
Convert visitors into leads and customers.

**Features**
- Course / Batch / Webinar listing
- Registration & Login
- Direct purchase (Courses, Webinars)
- Batch enquiry form → CRM
- Scholarship & Entrance test registration
- Campaign landing pages
- Basic search & filters

**Excluded (Phase-2)**
- AI recommendation quiz  
- Skill path visualizations  
- Personalization engines  


### 2. CRM Dashboard – *Sales + Communication Command Center*

**Purpose:**  
Single source of truth for **Leads, Students, Payments, and Communications**.

#### A. Lead Management
- Lead list & filters
- Lead profile with activity timeline
- Manual lead creation
- Lead assignment to PROs
- Status pipeline:
  - New → Contacted → Interested → Converted → Lost

#### B. Student Management
- Student directory
- 360° student profile:
  - Lead history
  - Payment history
  - LMS enrollment
  - Communication logs

#### C. Payment & Finance
- Razorpay payment sync
- Offline payment entry
- Invoice generation
- Refund status tracking
- Payment communication history

#### D. Communication Hub (Simplified)
- Unified inbox: Email + SMS + WhatsApp
- Message templates
- Manual & bulk messaging
- Delivery & response status

#### E. Webinar & Campaign Management
- Webinar listing
- Registration tracking
- Manual reminders & follow-ups
- Attendance import

#### F. Business Dashboard
- Total leads
- Conversion rate
- Revenue
- Webinar performance

**Excluded**
- AI communication suggestions  
- Voice calling  
- Advanced marketing automation  
- Predictive analytics  



### 3. LMS User App – *Learning Execution System*

**Purpose:**  
Deliver training programs, tests, and internships reliably.

#### A. Unified Dashboard
- My Batches
- My Courses
- My Tests
- My Webinars

#### B. Learning Modules
- Live class access (Zoom/Meet)
- Recorded session playback
- Notes & resources
- Attendance tracking
- Assignment upload
- Quiz participation

#### C. Test Platform (Critical)
Supports:
- Scholarship Tests
- Competitive Exams
- Entrance Tests

**Anti-Cheating (MVP)**
- Fullscreen enforcement
- Tab switching detection
- Timer enforcement
- IP logging
- Optional camera permission

**Excluded**
- AI proctoring
- Facial recognition
- Virtual invigilation

#### D. Communication (MVP)
- Announcements system

**Excluded**
- Community chat
- Doubt forum
- AI doubt solver


### 4. LMS Admin Dashboard – *Academic Control System*

**Purpose:**  
Operate the education engine.

**Features**
- Course / Batch CRUD
- Faculty assignment
- Student enrollment (bulk)
- Content upload
- Quiz/Test creation
- Assignment evaluation
- Attendance view

**Excluded**
- Faculty analytics
- Community moderation
- Engagement scoring



## 🔧 Technology Stack

| Layer | Technology |
|------|----------|
| Web Apps | Next.js 16 (App Router) |
| Mobile LMS | React Native (Expo) |
| Backend & Auth | Supabase (PostgreSQL + Auth) |
| File Storage | Supabase Storage |
| Realtime | Supabase Realtime |
| Background Jobs | Bull + Redis |
| Payments | Razorpay |
| Email | Resend |
| SMS / WhatsApp | MSG91 |
| Live Classes | Zoom / Google Meet |
| Deployment | Coolify |

---

## 🧭 Product Decisions Log

### Why These Are in MVP

| Feature | Reason |
|------|------|
| CRM Communication Hub | Direct impact on conversion |
| Scholarship Tests | Powerful lead acquisition |
| Anti-cheating test system | Brand trust |
| Invoice & payment logs | Financial accuracy |
| Unified student view | Operational clarity |
| Webinar module | Lead → Batch funnel |

---

### Why These Are Deferred

| Feature | Reason |
|------|------|
| AI recommendations | Requires data maturity |
| AI doubt solver | High complexity |
| Community chats | Moderation overhead |
| Gamification | Engagement layer, not revenue |
| Skill paths | UX polish |
| Predictive CRM | Needs historical data |


## 📌 Product Truth

Rankbook is not an “AI-first” product.  
It is a **revenue-first education system**.

AI will enhance:
- Personalization
- Support
- Analytics  

But only after:
- Sales workflows stabilize
- Education delivery is reliable
- Business metrics are consistent

---

## 🧩 Core Business Flow

```

Visitor → Lead → Payment → Student → Learning → Outcome → Revenue Tracking

```

Every feature must support this loop.

---

## 🏁 Status

This README defines the **true MVP boundary**.  
Anything outside this is Phase-2 or Phase-3.

This makes Rankbook:
- Buildable
- Fundable
- Maintainable
- Scalable

---

> “Discipline before intelligence.  
Execution before elegance.  
Business before beauty.”
```
