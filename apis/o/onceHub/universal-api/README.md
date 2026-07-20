# <img src="https://images.mindcloud.co/apps/icons/once-hub_1773245023842.png" alt="OnceHub logo" width="28" height="28"> OnceHub: Universal API

Manage bookings, scheduling resources, and webhooks in OnceHub

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onceHub/latest
- **Category:** Productivity / Scheduling
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.oncehub.com
- **Vendor API docs:** https://developers.oncehub.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | PUT |  |
| [Get Booking](actions/get-booking.md) | GET |  |
| [List Bookings](actions/list-bookings.md) | GET |  |
| [Request Booking Reschedule](actions/request-booking-reschedule.md) | PUT |  |
| [Set Booking No-Show](actions/set-booking-no-show.md) | PUT |  |

### Booking Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Calendar](actions/get-booking-calendar.md) | GET |  |
| [List Booking Calendars](actions/list-booking-calendars.md) | GET |  |

### Booking Page

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Pages](actions/list-booking-pages.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET |  |

### Master Page

| Action | Method | Description |
| --- | --- | --- |
| [List Master Pages](actions/list-master-pages.md) | GET |  |

### One-time Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking Calendar One-Time Link](actions/create-booking-calendar-one-time-link.md) | POST |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

