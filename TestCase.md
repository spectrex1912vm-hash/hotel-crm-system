HOTEL CRM SYSTEM — TEST CASES



&#x20;

Hotel CRM System — система управления бронированиями, календарём, оплатами и AI автоматизацией.



\---



BOOKING CRUD



TC-1 — Create Booking (POST)

Preconditions: user is authenticated



Steps:

1\. Open booking form

2\. Enter guest data

3\. Select dates

4\. Select room

5\. Click Create



Expected:

\- Booking is created

\- Appears in calendar

\- Saved in DB



\---



TC-2 — Get Booking (GET)

Steps:

GET /api/bookings/:id



Expected:

\- 200 OK

\- Correct booking object returned



\---



TC-3 — Update Booking (PUT)

Expected:

\- Data updated in DB

\- UI reflects changes



\---



TC-4 — Delete Booking (DELETE)

Expected:

\- Booking removed from system



\---



&#x20;CALENDAR



&#x20;TC-5 — Split-day booking logic

Steps:

\- Booking A checkout = 20 May

\- Booking B checkin = 20 May



Expected:

\- Both bookings allowed

\- Day visually split



\---



TC-6 — Calendar rendering

Expected:

\- No overlap bugs

\- Correct color mapping



\---



TC-7 — Overlapping protection

Expected:

\- Prevent invalid overlaps (except split-day)



\---



PAYMENTS



TC-8 — Partial payment

Expected:

\- status = partially paid



TC-9 — Full payment validation

Expected:

\- totalPaid == totalPrice → Paid



TC-10 — Debt calculation

Expected:

\- correct remaining balance



\---



&#x20;AI FEATURES



TC-11 — AI email parsing

Expected:

\- email → JSON → booking created



TC-12 — AI offline fallback

Expected:

\- CRM still works without AI



TC-13 — AI report generation

Expected:

\- summary of arrivals/departures/debts



&#x20;TC-14 — AI must not block UI

Expected:

\- manual input always works



\---



&#x20;ROOMS



TC-15 — Change room status

Expected:

\- status updates instantly



TC-16 — Room statuses

\- free / occupied / cleaning / ready / repair



TC-17 — AI room status button

Expected:

\- full system overview



\---



API TESTS (POSTMAN)



TC-18 — GET all bookings

GET /api/bookings

Expected: 200



TC-19 — CREATE booking

POST /api/bookings

Expected: 201



&#x20;TC-20 — UPDATE booking

PUT /api/bookings/:id

Expected: 200



TC-21 — DELETE booking

DELETE /api/bookings/:id

Expected: 200



\---



&#x20;ADVANCED TESTS



TC-22 — Race condition booking

Expected:

\- no duplicate overlaps under parallel requests



TC-23 — Email deduplication

Expected:

\- same email processed once only



TC-24 — AI provider switching

Expected:

\- Ollama / LM Studio / Claude interchangeable



TC-25 — System recovery

Expected:

\- service recovers after AI failure



