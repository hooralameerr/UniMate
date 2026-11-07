ADR-01: Booking Conflict Prevention

Status: Accepted

Related Requirement: FR-07.1

Context
UniMate must prevent tutors from having overlapping confirmed tutoring sessions.

Options Considered
1. Server-side booking validation.
2. Client-side booking validation.

Decision
Use server-side booking validation to check scheduling conflicts before confirming tutoring sessions.

Trade-off
Server-side validation enforces booking rules centrally and prevents clients from bypassing the checks. However, it requires additional backend processing and database queries.

Consequences
The Backend API will be responsible for validating session availability and preventing conflicting confirmed bookings.
