# <img src="https://images.mindcloud.co/apps/icons/r-fav_1776820655409.png" alt="Restoplace logo" width="28" height="28"> Restoplace: Universal API

Manage reservations, booking widgets, deposits, tickets, and guest communications in Restoplace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/restoplace/latest
- **Category:** Productivity / Scheduling
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://restoplace.cc/
- **Vendor API docs:** https://restoplace.cc/help/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Address Info](actions/get-address-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-address-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create Reservation](actions/create-reservation.md) | POST | Creates a new reservation in Restoplace. |
| [Get Reservation](actions/get-reservation.md) | GET | Retrieves a reservation from Restoplace. |
| [List Reservations](actions/list-reservations.md) | GET | Retrieves reservations from Restoplace. |
| [Update Reservation](actions/update-reservation.md) | PUT | Updates an existing reservation in Restoplace. |
| [Update Reservation Status](actions/update-reservation-status.md) | PUT | Updates a reservation status in Restoplace. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Item Types](actions/list-item-types.md) | GET | Retrieves item types from Restoplace. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Restoplace. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Item](actions/get-booking-item.md) | GET | Retrieves a booking item from Restoplace. |
| [List Booking Items](actions/list-booking-items.md) | GET | Retrieves booking items from Restoplace. |
| [Update Booking Item](actions/update-booking-item.md) | PUT | Updates an existing booking item in Restoplace. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Info](actions/get-address-info.md) | GET | Retrieves address information from Restoplace. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Hall](actions/get-hall.md) | GET | Retrieves a hall from Restoplace. |
| [List Halls](actions/list-halls.md) | GET | Retrieves halls from Restoplace. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Deposit](actions/calculate-deposit.md) | GET | Calculates a deposit in Restoplace. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Available Times](actions/list-available-times.md) | GET | Retrieves available booking times from Restoplace. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Reservation Cancel Reasons](actions/list-reservation-cancel-reasons.md) | GET | Retrieves reservation cancel reasons from Restoplace. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Restoplace. |

