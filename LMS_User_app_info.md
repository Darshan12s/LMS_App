# **LMS User App Project Charter (Aligned with Rankbook FSD MVP)**

## **Project Meta**

| **Attribute** | **Details** |
| --- | --- |
| **Project Name** | Rankbook LMS - Student Learning App |
| **Platform** | Cross-platform (Web, iOS, Android) |
| **Owner** | Head of Education |
| **Status** | 🟡 Planning |
| **Project ID** | RKB-LMS-STUDENT-MVP-001 |
| **Phase** | MVP (Minimum Viable Product) |

---

## **1. Project Vision**

**Build the simplest possible app that allows students to access their courses, attend live sessions, and submit assignments, enabling Rankbook to deliver education reliably.**

**Primary Goal:** Provide frictionless access to learning content for paying students.
**Secondary Goal:** Support basic cohort interaction without moderation burden.
**Non-Goal:** Building a social learning platform or advanced engagement features.

---

## **2. Guiding Principles (From Rankbook FSD)**

1. **Delivery First:** Focus on core learning delivery (videos, live sessions, assignments)
2. **Reliability > Features:** 100% uptime for live sessions beats fancy UI features
3. **Mobile Consumption:** Optimize for mobile learning consumption (not creation)
4. **Simple Communication:** One-way announcements only, no open forums in MVP

---

## **3. MVP Scope - STRICTLY LIMITED**

### **IN SCOPE (MVP)**

#### **A. Authentication & Onboarding**
- Login/Logout
- Password reset
- Profile viewing (read-only)

#### **B. Unified Dashboard**
- "My Learning" section showing:
  - Active Batches (Cohort-based)
  - Enrolled Courses (Self-paced)
  - Upcoming Webinars
  - Recent Activity
- Simple progress indicators (% complete)

#### **C. Batch Learning Interface**
- **Live Class Access:** Join Zoom/Google Meet via direct link
- **Recordings:** Watch past session recordings (YouTube embeds)
- **Resources:** Download/view PDFs, slides, notes
- **Attendance:** Automatic marking when joining live session
- **Basic Progress Tracking:** Mark lessons as complete

#### **D. Course Learning Interface (Self-paced)**
- Video player (YouTube embed)
- Course content structure (modules → lessons)
- Progress tracking (mark as complete)
- Downloadable resources

#### **E. Test Platform (Critical - Lead Generation)**
- **Entrance/Scholarship Tests:**
  - Full-screen enforcement
  - Tab switch detection (warning)
  - Timer with auto-submit
  - Basic question types (MCQ, descriptive)
- **Results:** Immediate score for objective tests
- **NO advanced proctoring** (camera, AI monitoring)

#### **F. Assignment Submission**
- Upload files (PDF, Word, images)
- View submission status
- See grades/comments (when graded)
- **NO peer review, NO advanced feedback tools**

#### **G. Announcements System (ONE-WAY ONLY)**
- View announcements per batch/course
- Mark as read/unread
- **NO replies, NO comments, NO student posting**

#### **H. Webinar Participation**
- View upcoming webinars
- Join live webinar (external link)
- Access recordings post-webinar
- Download resources

### ** OUT OF SCOPE (V2+)**
- Community chats
- Threaded Q&A forums
- Peer-to-peer messaging
- AI doubt solver
- Gamification (XP, badges, leaderboards)
- Advanced analytics dashboard
- Note-taking within app
- Video playback speed control
- Download videos for offline
- Calendar integration
- Push notifications
- In-app video player (beyond YouTube embed)
- Screen sharing
- Whiteboard tools
- Group projects
- Certificate generation
- Parent/guardian access
- Multi-language support

---

## **4. Success Criteria (MVP)**

### **Student Outcomes:**
1. **Access reliability:** 99% success rate joining live sessions
2. **Content consumption:** 80% of students watch >70% of videos
3. **Assignment submission:** >90% submission rate for assignments
4. **Test completion:** <5% test abandonment due to technical issues

### **Business Outcomes:**
1. **Support reduction:** <5 tickets per 100 students per week
2. **Batch completion:** >75% of students complete their batch
3. **Referral rate:** >10% of students refer others (measured via survey)
4. **Renewal intent:** >60% would enroll in another course (survey)

### **Technical Outcomes:**
1. **App load time:** <3 seconds
2. **Video load time:** <5 seconds
3. **Uptime:** 99% availability
4. **Crash rate:** <1% of sessions

---

## **5. Technical Stack (Minimal)**

| **Component** | **Technology** | **Why** |
| --- | --- | --- |
| **Framework** | React Native (Expo) | Cross-platform, faster development |
| **Navigation** | React Navigation | Standard for RN |
| **State Management** | React Query + Zustand | Simple, effective for API caching |
| **Video Player** | React Native YouTube Iframe | Reliable, handles DRM |
| **File Upload** | Expo Document Picker + Supabase Storage | Simple, already in stack |
| **Database/Auth** | Supabase SDK | Already in stack |
| **Push Notifications** | **Deferred to V2** | Complexity high for MVP |
| **PDF Viewer** | react-native-pdf | Lightweight |
| **Testing** | Jest + Detox | Basic testing |
| **Distribution** | Expo Application Services | Simplifies deployment |

---

## **6. Core User Flows (MVP Only)**

### **Flow 1: Student's Daily Learning**
1. Student opens app, sees "My Learning" dashboard
2. Sees today's live session (starts in 30 minutes)
3. Clicks on batch → sees resources for today's topic
4. 30 minutes later: clicks "Join Live Class" → opens Zoom/Meet
5. After class: marks attendance automatically
6. Downloads PDF resources
7. Checks if any assignments due

### **Flow 2: Taking a Scholarship Test**
1. Student sees "Scholarship Test Available" on dashboard
2. Clicks "Start Test" → full-screen mode activates
3. Timer starts, tab switching detection enabled
4. Answers questions (MCQ, text input)
5. Submits → sees immediate score (if objective)
6. Gets notification when results finalized

### **Flow 3: Submitting Assignment**
1. Student sees assignment in batch section
2. Clicks "Submit Assignment" → chooses file
3. Uploads PDF/Word file
4. Sees "Submitted" status
5. Later: sees grade and comments from faculty

### **Flow 4: Self-Paced Course Progress**
1. Student clicks on course in dashboard
2. Views course structure (modules → lessons)
3. Watches video (YouTube embed)
4. Marks lesson as "Complete"
5. Progress bar updates
6. Downloads supplementary materials

---

## **11. Risks & Mitigation**

| **Risk** | **Impact** | **Probability** | **Mitigation** |
| --- | --- | --- | --- |
| **Live session join failures** | High | Medium | Clear instructions, backup links |
| **Video playback issues** | High | Medium | YouTube embed (most reliable) |
| **File upload failures** | Medium | Medium | Retry logic, size limits |
| **Test platform cheating** | Medium | High | Accept in MVP, manual review of top scores |
| **App store rejection** | High | Low | Follow guidelines, test thoroughly |
| **Android fragmentation** | Medium | High | Test on 3 key Android versions |

---

## **12. Definition of Done**

### **For MVP Launch:**
1. ✅ Students can join live sessions reliably
2. ✅ Videos play without major issues
3. ✅ Assignments can be submitted
4. ✅ Tests can be taken with basic anti-cheating
5. ✅ Progress is tracked accurately
6. ✅ Works on iOS and Android
7. ✅ App store deployed
8. ✅ 20+ students successfully tested

### **Technical DoD:**
1. ✅ App size < 50MB
2. ✅ Cold start < 3 seconds
3. ✅ Video load < 5 seconds
4. ✅ No memory leaks
5. ✅ Offline handling (graceful errors)
6. ✅ Back button works correctly

---

## **13. Key Decisions & Constraints**

### **Decisions:**
1. **No in-app video calls** → Open Zoom/Meet externally
2. **No push notifications** → Use email/SMS for critical alerts
3. **No chat/forums** → One-way announcements only
4. **No offline videos** → Streaming only
5. **No iOS/Android specific features** → Common codebase only

### **Constraints:**
1. **Devices:** Support last 2 iOS versions, Android 10+
2. **Network:** Optimize for 3G+ connections
3. **Storage:** Keep app under 50MB download
4. **Testing:** Manual testing only, no automated CI/CD for mobile
5. **Users:** Max 500 concurrent students in MVP

---



### **iOS:**
- iOS 14.0 or later
- iPhone 8 or later
- 2GB RAM minimum

### **Android:**
- Android 10 (API 29) or later
- 3GB RAM recommended
- Chrome browser installed

### **Web:**
- Chrome 80+, Safari 14+, Edge 80+
- 5MBps internet for video
- 1024×768 screen minimum

---

*Document Version: 2.0 (Aligned with Rankbook FSD)*  
*Last Updated: [Current Date]*  
*Next Review: After 8 weeks (MVP launch)*  
*Distribution: Core team only*