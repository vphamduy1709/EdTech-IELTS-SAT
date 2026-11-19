# IELTS Test Prep Platform (MVP)

A web platform that helps IELTS teachers manage classes, author Reading and Writing tests, assign deadlined homework, and grade Writing against the 4-criteria IELTS rubric. Students take tests in an interface that mirrors IELTS on Computer, and their work is not lost when the network drops or the page reloads.

## Goals

- Replace the fragmented workflow (Zalo, Google Forms, Google Docs) with a single platform for IELTS classes.
- Help teachers author tests, assign work, and grade Writing faster and more consistently against the IELTS rubric.
- Give students a test-taking experience close to the real exam, without the risk of losing progress when the connection is unstable.

## Features

### Class Management
- Create, edit, and archive classes with a name, description, and target band.
- Each class has a 6-character join code; teachers can regenerate it.
- Students join a class with the code and can belong to multiple classes.
- Teachers view the class roster and remove students.
- Create class sessions with date, start and end time, and a Google Meet or Zoom link; students see their upcoming sessions and open the room link from the platform.

### Test Authoring
- Reading tests with 1 to 3 passages, each containing question groups with instructions.
- Writing Task 2 tests with a prompt and a minimum word count.
- Three question types: Multiple Choice, True/False/Not Given (including Yes/No/Not Given), and Gap Fill with a word limit.
- The input form changes with the question type; question numbers renumber automatically when questions are added, removed, or reordered.
- Tests have Draft and Published states. A test with missing answers cannot be published, and the problem questions are flagged.

### Assignments
- Assign a published test to a class with an open time, a deadline, and a time limit.
- The system blocks starting outside the open window and closes the gate automatically after the deadline.
- Students see each assignment's status: Not yet open, Open, Submitted, Graded, or Overdue.
- Teachers see who has submitted, when, the score, and who has not submitted.

### Test Taking
- Split-view Reading interface with the passage on the left and questions on the right, with a draggable divider.
- Writing interface with the prompt on the left, an editor on the right, and a live word counter.
- Countdown timer that turns to a warning color when 5 minutes remain.
- Question navigator in the footer showing answered, unanswered, and marked-for-review questions, with click-to-jump.
- Students can mark individual questions for review.
- Every change is auto-saved; students can keep working while offline, and changes sync automatically once the connection returns.
- Reloading the page, or signing in on another device, returns the student to the same attempt with answers and remaining time restored.
- Submission asks for confirmation and shows how many questions are unanswered.
- When time runs out, the attempt is submitted automatically, even if the device has disconnected.

### Grading and Results
- Reading is graded automatically on submission and converted to a band score.
- Writing is graded on four criteria (TR, CC, LR, GRA), each scored 0 to 9 in steps of 0.5, with written feedback.
- The overall band is calculated and rounded using IELTS rounding rules.
- Teachers can save grades as drafts or publish them; students see Writing scores only after publication.
- After the deadline, students can review Reading answers with correct and incorrect markings for each question.

### Student Home
- Shows upcoming deadlines and upcoming class sessions.

### Planned Extensions (SHOULD)
- AI-assisted Writing feedback, where the teacher always makes the final scoring decision.
- Class dashboard with submission rates and average bands per assignment.
- Band trend charts for Reading and Writing over time.
- CSV export of class results.
- Per-student session notes written by teachers after a class.
- Matching Headings question type.
- In-app notifications for new assignments, graded Writing, and approaching deadlines.

## Quality Guarantees

- **No lost work:** each change is saved on the device within 1 second and synced to the server within 10 seconds.
- **Reliable timing:** the server controls the exam clock, so changing the device's clock has no effect; late submissions are accepted for up to 30 seconds to absorb network delay.
- **Protected answers:** test data sent to students never includes answers; answers are revealed only after the deadline.
- **Server-side access control:** students can only see classes they have joined, enforced by the backend and not just by hiding UI elements.
- **AI is optional:** all core features keep working when the AI service is turned off.

## Supported Environment

- Browsers: latest Chrome, Edge, and Firefox; Safari on a best-effort basis.
- Test-taking interface: desktop only, minimum screen size 1280 × 720.

## Roadmap Beyond MVP

Digital SAT, IELTS Listening and Speaking, a daily practice module with streaks and flashcards, competency charts, and multi-tenant support for multiple test prep centers.
