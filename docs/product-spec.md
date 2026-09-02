# Student OS — Product Specification

## 1. Product Overview

Student OS is a personal academic management platform designed for university students.

The platform helps students organize their semester, manage courses and schedules, prepare for exams, track academic progress, manage study materials and questions, and collaborate with other students.

The goal is to provide students with one central workspace for their academic life throughout the semester.

---

## 2. Target Users

The primary users are university students.

A student should be able to create an account, configure their academic information, create a semester, add their courses and schedule, and use the platform throughout the semester.

---

## 3. Core Product Features

### 3.1 Authentication

Students can:

* Create an account with email and password
* Sign in
* Sign out
* Continue with Google
* Reset their password
* Manage their authenticated session

Each account belongs to one student.

---

### 3.2 Student Profile

Students can manage their academic profile.

Profile information may include:

* Full name
* Username
* University
* Faculty
* Major
* Group
* Academic year
* Current semester

The profile is used to personalize the student's academic workspace.

---

### 3.3 University

The platform stores university information.

A student can select their university during profile or semester setup.

The system should support multiple universities so the platform can grow beyond a single institution.

University-related information may include:

* University name
* Faculty
* Major
* Groups
* Available courses

---

### 3.4 Semester

A student can create and manage an academic semester.

A semester contains:

* Academic year
* Semester name
* Courses
* Schedule
* Tasks
* Exams
* Study progress

The student can initially edit their semester setup.

When the schedule and semester information are confirmed, the student can mark the semester as confirmed.

The confirmed semester becomes the student's active academic structure.

The system should still allow controlled editing when necessary.

---

### 3.5 Courses

Students can add courses to their semester.

Each course has its own workspace.

A course can contain:

* Course name
* Instructor
* Credits
* Schedule
* Topics
* Tasks
* Materials
* Questions
* Exam questions
* Study sessions
* Progress

---

### 3.6 Schedule

Students can create their weekly university schedule.

A schedule item can contain:

* Course
* Day
* Start time
* End time
* Classroom
* Instructor
* Additional notes

The dashboard uses the schedule to display:

* Today's classes
* Upcoming classes
* Next class

The schedule should be responsive and easy to use on mobile devices.

---

### 3.7 Dashboard

The dashboard is the student's main workspace.

It provides a personalized overview of the semester.

The dashboard may display:

* Today's classes
* Next class
* Upcoming tasks
* Upcoming exams
* Course progress
* Study progress
* Recently added questions
* Important notifications
* Recommended activities

The dashboard should prioritize information that requires the student's attention.

---

### 3.8 Tasks

Students can create academic tasks.

A task can contain:

* Title
* Description
* Course
* Deadline
* Priority
* Status
* Notes

Possible statuses:

* Pending
* In progress
* Completed

Students can view upcoming and completed tasks.

---

### 3.9 Materials

Students can organize study materials by course and topic.

Materials may include:

* PDFs
* Documents
* Links
* Notes
* External resources

Students may save links to external platforms such as Google Classroom.

Future versions may support integrations with external academic platforms.

---

### 3.10 Questions

Students can create questions while studying.

A question belongs to a course and may optionally belong to a topic.

Questions can be:

* Private
* Shared with the community

A student can track whether a question has been:

* Unanswered
* In progress
* Resolved

Students should be able to add notes and explanations to their questions.

---

### 3.11 Exam Questions

Students can organize and track exam questions.

An exam question can contain:

* Course
* Topic
* Question text
* Source
* Personal answer
* Correct answer or explanation
* Status

Students can track:

* Total questions
* Solved questions
* Unsolved questions
* Correct answers
* Incorrect answers
* Reviewed questions

Example:

```text
Database Exam

Total:       40
Solved:      27
Correct:     21
Incorrect:    6
Unsolved:    13
```

This information contributes to exam preparation progress.

---

### 3.12 Study Sessions

Students can record individual study sessions.

A study session can contain:

* Course
* Topic
* Start time
* End time
* Duration
* Notes
* Difficulty
* Completed activities

Study sessions contribute to academic analytics.

---

### 3.13 Progress

The platform tracks student progress.

Progress can be calculated at different levels:

```text
Semester
    ↓
Course
    ↓
Topic
    ↓
Study activity
```

Examples of tracked activities:

* Completed tasks
* Studied topics
* Solved questions
* Reviewed mistakes
* Completed study sessions
* Exam preparation

The system should provide a clear visual representation of progress.

---

### 3.14 Analytics

Analytics provide an overview of the student's academic activity.

Possible analytics include:

* Total study time
* Study time by course
* Course progress
* Topic progress
* Task completion
* Exam preparation
* Question accuracy
* Most difficult topics
* Most active study days

Analytics should help students understand where they are spending their time and where they need more preparation.

---

### 3.15 Community

Student OS includes a student academic community.

Students can:

* Create public questions
* Answer questions
* Comment on discussions
* Share useful resources
* Search existing questions
* Discuss courses and topics

Community content should be connected to academic entities such as:

* University
* Course
* Topic

The community should remain focused on academic collaboration.

---

### 3.16 Notifications

The system can notify students about important academic events.

Possible notifications include:

* Upcoming class
* Upcoming task deadline
* Upcoming exam
* Unfinished tasks
* Community responses
* Study reminders

Notifications may initially be displayed inside the application.

External notifications can be introduced later.

---

### 3.17 Integrations

The platform may integrate with external services.

Planned integrations include:

* Google OAuth
* Google Calendar
* Google Classroom

Integrations should be implemented separately from the core academic system so that the platform can continue functioning if an external service is unavailable.

---

## 4. Main User Flow

The primary student flow is:

```text
Landing Page
      ↓
Sign Up / Sign In
      ↓
Student Profile Setup
      ↓
University / Major / Group
      ↓
Create Semester
      ↓
Add Courses
      ↓
Create Schedule
      ↓
Review Schedule
      ↓
Confirm Semester
      ↓
Personal Dashboard
      ↓
Manage Semester
```

During the semester:

```text
Dashboard
    ↓
Classes
Tasks
Materials
Questions
Exam Questions
Study Sessions
Progress
Community
    ↓
Analytics
```

---

## 5. Product Principles

### Personal First

Each student has their own private academic workspace.

### Academic Focus

The platform should focus on university life and studying rather than becoming a general social network.

### Simple Interaction

Common actions should require as few steps as possible.

### Mobile Friendly

Students should be able to use the platform comfortably from their phones.

### Data Connected

Information entered in one part of the platform should be useful in other parts.

For example:

```text
Schedule
   ↓
Dashboard

Exam Date
   ↓
Dashboard
   ↓
Study Planning

Exam Questions
   ↓
Progress
   ↓
Analytics
```

### Extensible

The system should be designed so that new universities, courses, integrations, and features can be added without rebuilding the entire application.

---

## 6. Platform Structure

The main product areas are:

```text
Student OS
│
├── Authentication
├── Student Profile
├── University
├── Semester
├── Courses
├── Schedule
├── Dashboard
├── Tasks
├── Materials
├── Questions
├── Exam Questions
├── Study Sessions
├── Progress
├── Analytics
├── Community
├── Notifications
└── Integrations
```

---

## 7. Initial Scope

The first working version should establish the core academic system:

```text
Authentication
        ↓
Student Profile
        ↓
Semester
        ↓
Courses
        ↓
Schedule
        ↓
Dashboard
        ↓
Tasks
        ↓
Questions
        ↓
Exam Questions
        ↓
Progress
```

Community, analytics, notifications, and external integrations will be built on top of this core system.

---

## 8. Long-Term Vision

Student OS should become a complete digital academic workspace for university students.

The platform should eventually help a student answer:

* What classes do I have today?
* What do I need to do?
* What should I study next?
* How prepared am I for my exams?
* Which topics am I struggling with?
* What materials do I need?
* How much have I studied?
* Where can I ask a question?
* What have I completed this semester?

The long-term goal is to replace fragmented academic workflows with one connected student workspace.
