ADR-02: Mock Reminder Scheduling

Status: Accepted

Related Requirements: FR-09.1, FR-09.2, NFR-07.1

Context
UniMate must generate mock notifications and scheduled reminders for tutoring sessions. Confirmed sessions require reminders 24 hours and 1 hour before their scheduled start times.

Options Considered
1. Background scheduler.
2. Check reminders only when users open the application.

Decision
Use a background scheduler to manage mock reminders for confirmed tutoring sessions.

Trade-off
A background scheduler can process reminders at their scheduled times without relying on users opening the application. However, it requires a continuously running process and additional scheduling logic.

Consequences
UniMate will include a background scheduling component that checks confirmed sessions and creates mock reminders when they are due.
