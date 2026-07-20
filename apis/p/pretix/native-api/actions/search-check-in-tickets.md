# Search Check In Tickets with pretix

Searches check-in tickets in pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/checkinrpc/search/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Search Check In Tickets](https://docs.pretix.eu/dev/api/resources/checkin.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `list` | query | `string` | yes | Check-in list ID to search within. |
| `search` | query | `string` | yes | Ticket, attendee, or order search text. |
