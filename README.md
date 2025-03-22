# Movie Seat Reservation Coding Task 

You're building a movie theater seat reservation system (using Next.js).
There are five fixed seats: A1–A5.

When a user selects an available seat, it is temporarily reserved for 5 minutes. If not confirmed, the seat becomes available again.

## API Requirements (Backend):

`GET /api/seats`
Returns current availability for all seats (available, reserved, or taken).

`POST /api/reserve-seat`
Inputs: seatId, userId
Temporarily reserves a seat if available.

`POST /api/confirm-seat`
Inputs: seatId, userId
Confirms the temporary reservation permanently if still valid.

## Frontend Requirements (React/Next.js):

Fetch seat status from /api/seats.

Display seats with clear indicators:
- 🟩 Available (for selection)
- 🟨 Temporarily reserved by current user (with countdown)
- 🟥 Unavailable (taken or reserved by others)

Allow user to select and confirm a seat.

Data Storage:

Use a simple in-memory JavaScript object (no database needed).

Each seat has minimal attributes:
status, reservedBy, expiresAt

Testing clearly explained:
Describe verbally how you'd test concurrency (e.g., two browsers).
