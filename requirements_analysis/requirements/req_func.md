You're absolutely right. Removed the timeline assumptions. Here's the corrected version:

# Functional Requirements for ADHD Application

🔙 [Back](./README.md)

## 🎯 Objective
Define the specific features and capabilities the ADHD application will provide, based on user research and personas. These are the "what" - what the system does for users.

---

## 📱 Core Application Features

### **F1: Micro-Task Management System**

#### **F1.01 - Automatic Task Breakdown**
**Description:** Automatically decomposes overwhelming tasks into manageable 5-15 minute micro-tasks  
**User Story Reference:** #1 (Alex - task paralysis)  
**Acceptance Criteria:**
- User can input any task with description
- System suggests 3-5 micro-tasks based on task type and past patterns
- Each micro-task displays estimated time and priority
- Progress is visually tracked (e.g., "2/5 completed")
- User can modify or reject suggested breakdown
- **MVP:** Yes | **Priority:** Critical

#### **F1.02 - One-Click Task Initiation**
**Description:** Start any task with minimal friction  
**User Story Reference:** #1 (Alex - overcoming "wall of awful")  
**Acceptance Criteria:**
- Each micro-task has prominent "Start Now" button
- Starting a task automatically begins focus timer
- Interface simplifies to single-task view during execution
- Cannot start new tasks until current completes or is cancelled
- **MVP:** Yes | **Priority:** Critical

#### **F1.03 - Task Template Library**
**Description:** Pre-built templates for common ADHD challenges  
**User Story Reference:** #7 (Sophie - email anxiety), #13 (Chen family - morning routine)  
**Acceptance Criteria:**
- Templates include: Email writing, Morning routine, Study session, Meeting preparation
- Users can save and share custom templates
- Templates auto-populate with user's frequent tasks
- **MVP:** No | **Priority:** Medium

### **F2: ADHD-Friendly Time Management**

#### **F2.01 - Visual Pomodoro Timer**
**Description:** Time representation optimized for ADHD time blindness  
**User Story Reference:** #4 (Marcus - 4-hour lectures), #5 (Isabella - grading marathons)  
**Acceptance Criteria:**
- Circular timer that visually shrinks as time elapses
- Color transitions: Green → Yellow → Red as period ends
- Gentle vibration at transitions (optional)
- Shows remaining time in words: "15 minutes left"
- **MVP:** Yes | **Priority:** Critical

#### **F2.02 - Smart Break System**
**Description:** Intelligent break suggestions to maintain momentum  
**User Story Reference:** #11 (Marcus - movement needs)  
**Acceptance Criteria:**
- Auto-schedules breaks after focus sessions
- Suggests break types: Movement, Hydration, Snack, Rest
- Rotates suggestions to prevent habituation
- Optional "skip break" with gentle encouragement
- **MVP:** Yes | **Priority:** High

#### **F2.03 - Time Buffer Automation**
**Description:** Automatically adds buffer time between tasks  
**User Story Reference:** #3 (Carlos - interruptions), #6 (David - travel time)  
**Acceptance Criteria:**
- Detects task transitions and location changes
- Adds 25-50% buffer time based on task type
- Learns from user's actual vs estimated times
- **MVP:** No | **Priority:** Medium

### **F3: Medication & Wellness Management**

#### **F3.01 - Medication Tracking**
**Description:** Simple medication reminder and confirmation system  
**User Story Reference:** #12 (Chen family - medication coordination), #23 (Marcus - meal reminders)  
**Acceptance Criteria:**
- Custom schedules per medication
- "Taken" confirmation with timestamp
- "Snooze" option (15min, max 3x)
- 7-day visual history
- No medical advice - reminder function only
- **MVP:** Yes | **Priority:** Critical

#### **F3.02 - Family Medication Dashboard**
**Description:** Shared view for family medication management  
**User Story Reference:** #12 (Chen family - avoid double dosing)  
**Acceptance Criteria:**
- Parents see child's medication status only
- Status indicators: ✅ Taken, ⏰ Pending, ❌ Missed
- No sensitive medical details shared
- Emergency override available
- **MVP:** No | **Priority:** High (if doing family features)

### **F4: Focus & Distraction Control**

#### **F4.01 - Selective App Blocking**
**Description:** Block distracting apps during focus sessions  
**User Story Reference:** #2 (Elena - rabbit hole prevention)  
**Acceptance Criteria:**
- User-selectable apps to block
- Always-allow list (Phone, Messages, Maps)
- "Emergency override" with 3-second hold
- Statistics on blocked distraction attempts
- **MVP:** Yes | **Priority:** High

#### **F4.02 - "Low Spoons" Mode**
**Description:** Simplified interface for high-symptom days  
**User Story Reference:** #10 (All personas - bad ADHD days)  
**Acceptance Criteria:**
- One-button activation from any screen
- Shows only: Timer, Medication, Break buttons
- Extra large touch targets and text
- No complex features or decisions required
- **MVP:** Yes | **Priority:** High

### **F5: Emotional & Psychological Support**

#### **F5.01 - RSD Email Assistant**
**Description:** Helps manage rejection-sensitive dysphoria in communication  
**User Story Reference:** #7 (Sophie - client email anxiety)  
**Acceptance Criteria:**
- Email draft analyzer for self-critical language
- Suggests neutral alternative phrasing
- "Send later" scheduling to reduce anxiety
- Template responses for common scenarios
- **MVP:** No | **Priority:** Medium

#### **F5.02 - Progress Celebration**
**Description:** ADHD-appropriate achievement recognition  
**User Story Reference:** #9 (Robert - small wins), #26 (Alex - sleep routine)  
**Acceptance Criteria:**
- Visual feedback on task completion
- Weekly summary of accomplishments
- No streak-based systems (avoids shame)
- Optional sharing to accountability partner
- **MVP:** Yes | **Priority:** Medium

### **F6: Accessibility & Usability**

#### **F6.01 - Voice Command Interface**
**Description:** Hands-free operation for various contexts  
**User Story Reference:** #17 (David - dirty hands on construction site)  
**Acceptance Criteria:**
- "Start 25-minute timer for [task]"
- "Log medication taken"
- "Add task: [description]"
- Works offline for core commands
- **MVP:** No | **Priority:** Medium

#### **F6.02 - Offline-First Architecture**
**Description:** Core functions work without internet  
**User Story Reference:** #19 (Carlos - poor farm reception)  
**Acceptance Criteria:**
- Timer functions fully offline
- Task lists available offline
- Auto-sync when connection restored
- Clear offline status indication
- **MVP:** Yes | **Priority:** Critical

---

## 📊 Feature Prioritization

### **Critical Priority (Must Have for MVP)**
- F1.01: Automatic Task Breakdown
- F1.02: One-Click Task Initiation  
- F2.01: Visual Pomodoro Timer
- F3.01: Medication Tracking
- F4.02: "Low Spoons" Mode
- F6.02: Offline-First Architecture

### **High Priority (Important for Core Experience)**
- F2.02: Smart Break System
- F4.01: Selective App Blocking
- F5.02: Progress Celebration
- F3.02: Family Medication Dashboard (if family focus)

### **Medium Priority (Enhancements)**
- F5.01: RSD Email Assistant
- F2.03: Time Buffer Automation
- F6.01: Voice Command Interface
- F1.03: Task Template Library

---

## 🎯 User-Centric Feature Mapping

| Persona | Core Features | Success Metric |
|---------|--------------|----------------|
| **Alex** (Startup Founder) | F1.01, F1.02, F4.02 | Completes investor pitch prep on time |
| **Isabella** (Teacher) | F2.01, F2.02, F5.02 | Grades 120 papers with consistent quality |
| **Marcus** (Student) | F2.01, F3.01, F4.01 | Maintains focus through 4-hour lectures |
| **Sophie** (Artist) | F5.01, F4.02 | Sends client emails without 3-day delay |
| **David** (Construction) | F6.01, F2.03 | Tracks all site issues without losing notes |
| **Chen Family** | F3.01, F3.02 | Zero missed/double medication doses |

---

🔝 [Back to Top](#functional-requirements-for-adhd-application)