# card-counting-academy2
/docs/MASTER_SPEC.md
Card Counting Academy - Master Specification

Goal

Build a production-ready blackjack training platform for card counters.

Users can:

* Learn blackjack basic strategy
* Learn Hi-Lo card counting
* Learn true count conversion
* Learn deviations (Illustrious 18 + Fab 4)
* Practice in realistic simulations
* Take exams
* Earn certifications
* Track analytics and progress

⸻

Tech Stack

Monorepo

Frontend:

* React
* TypeScript
* Vite
* Tailwind
* Zustand
* React Query

Backend:

* NestJS
* TypeScript
* Prisma
* PostgreSQL
* Redis

Infrastructure:

* Docker
* GitHub Actions
* Sentry
* OpenTelemetry

⸻

Repository Structure

card-counting-academy/

apps/
web/
api/

packages/
blackjack-engine/
count-engine/
strategy-engine/
deviation-engine/
shared/

prisma/

docs/

.github/

⸻

Blackjack Engine

Support:

* 6 deck shoe
* configurable decks
* penetration
* dealer hits soft 17
* dealer stands soft 17
* blackjack payouts
* insurance
* surrender
* split
* double
* resplit
* bankroll tracking

Functions:

* createShoe()
* dealCard()
* evaluateHand()
* resolveHand()
* calculateEV()

⸻

Count Engine

Hi-Lo count system.

Values:

2-6 = +1
7-9 = 0
10-A = -1

Functions:

* runningCount()
* trueCount()
* decksRemaining()

⸻

Strategy Engine

Implement complete basic strategy.

Support:

* hard totals
* soft totals
* pair splits
* surrender

Return:

HIT
STAND
DOUBLE
SPLIT
SURRENDER

⸻

Deviation Engine

Implement:

Illustrious 18

Fab 4

Return optimal action based on true count.

⸻

Simulator

Features:

* live blackjack play
* count display
* optional hidden count
* bankroll tracking
* betting spread trainer
* session history

⸻

Analytics

Track:

* hands played
* win rate
* hourly EV
* profit
* bankroll
* count accuracy
* true count accuracy
* strategy accuracy
* deviation accuracy

⸻

Learning Center

Courses:

* Blackjack Basics
* Basic Strategy
* Hi-Lo Counting
* True Count Conversion
* Illustrious 18
* Fab 4
* Bankroll Management

Features:

* lessons
* quizzes
* drills
* progress tracking
* XP
* levels

⸻

Exams

Certifications:

1. Running Count Apprentice
2. Running Count Expert
3. True Count Expert
4. Basic Strategy Expert
5. Deviation Expert
6. Professional Card Counter

Requirements:

* randomized questions
* timers
* grading
* pass/fail
* certificates

⸻

Authentication

Features:

* register
* login
* forgot password
* JWT auth
* refresh tokens
* roles

⸻

Database

Prisma models:

User
Session
SimulatorSession
Course
Lesson
LessonProgress
Exam
ExamAttempt
Certification
Analytics

Use PostgreSQL.

⸻

Testing

Unit Tests:
95% coverage

Integration Tests:
95% coverage

E2E Tests:
Playwright

Test:

* auth
* simulator
* learning
* exams
* certifications
* analytics

⸻

Security

Implement:

* Helmet
* Rate limiting
* DTO validation
* Argon2 password hashing
* OWASP best practices

⸻

Deployment

Docker

Docker Compose

GitHub Actions

Production:

* PostgreSQL
* Redis
* HTTPS
* Backups
* Monitoring

⸻

Definition of Done

Application must:

* compile
* pass tests
* support all learning systems
* support all simulator systems
* support certifications
* support analytics
* be deployable with Docker