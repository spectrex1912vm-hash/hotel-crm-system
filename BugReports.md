HOTEL CRM BUG REPORTS



\---



BUG-1 — Form fields not editable

Severity: High



Actual Result:

User cannot type into input fields or values reset instantly.



Expected Result:

User can freely edit all booking fields.



\---



BUG-2 — AI overwrites manual input

Severity: High



Actual Result:

AI autofill replaces user input while typing.



Expected Result:

AI should only suggest, not override.



\---



BUG-3 — Calendar split-day issue

Severity: Medium



Actual Result:

Check-in/check-out same-day bookings overlap visually.



Expected Result:

Day is split visually into two bookings.



\---



BUG-4 — Payment calculation incorrect

Severity: High



Actual Result:

Partial payments not reflected correctly.



Expected Result:

Correct aggregation of payments.



\---



BUG-5 — Email duplication bug

Severity: Critical



Actual Result:

Same email creates multiple bookings.



Expected Result:

Deduplication by message ID.



\---



BUG-6 — AI service crash breaks CRM

Severity: High



Actual Result:

CRM stops working when AI offline.



Expected Result:

Graceful fallback mode.



\---



BUG-7 — Room status desync

Severity: Medium



Actual Result:

UI shows different status than DB.



Expected Result:

Single source of truth.



\---



BUG-8 — API inconsistent state

Severity: High



Actual Result:

GET returns outdated booking data.



Expected Result:

Consistent DB sync.



\---



BUG-9 — Race condition booking overlap

Severity: Critical



Actual Result:

Simultaneous requests create overlapping bookings.



Expected Result:

Atomic booking validation.



\---



BUG-10 — AI blocks UI interaction

Severity: High



Actual Result:

Form freezes during AI processing.



Expected Result:

UI remains responsive.



