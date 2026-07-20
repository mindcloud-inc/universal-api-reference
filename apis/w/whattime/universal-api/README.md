# <img src="https://images.mindcloud.co/apps/icons/whattime_1774277884194.png" alt="Whattime logo" width="28" height="28"> Whattime: Universal API

Manage bookings, calendars, availability, routing forms, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whattime/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whattime.co.kr
- **Vendor API docs:** https://developer.whattime.co.kr/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My User](actions/get-my-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Create Availability](actions/create-availability.md) | POST |  |
| [Delete Availability](actions/delete-availability.md) | DELETE |  |
| [Get Availability](actions/get-availability.md) | GET |  |
| [Get Basic Availability](actions/get-basic-availability.md) | GET |  |
| [List Availabilities](actions/list-availabilities.md) | GET |  |
| [Update Availability](actions/update-availability.md) | PUT |  |
| [Update Basic Availability](actions/update-basic-availability.md) | PUT |  |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | GET |  |
| [List Calendars](actions/list-calendars.md) | GET |  |
| [Upsert Calendar](actions/upsert-calendar.md) | PUT |  |

### Calendar Connection

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Connection](actions/create-calendar-connection.md) | POST |  |
| [Delete Calendar Connection](actions/delete-calendar-connection.md) | DELETE |  |
| [Get Calendar Connection](actions/get-calendar-connection.md) | GET |  |
| [List Calendar Connections](actions/list-calendar-connections.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Organization](actions/get-current-organization.md) | GET |  |

### Organization Member

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization Member](actions/delete-organization-member.md) | DELETE |  |
| [Get Organization Member](actions/get-organization-member.md) | GET |  |
| [Invite Organization Member](actions/invite-organization-member.md) | POST |  |
| [List Organization Members](actions/list-organization-members.md) | GET |  |
| [Update Organization Member](actions/update-organization-member.md) | PUT |  |

### Reservation

| Action | Method | Description |
| --- | --- | --- |
| [Get Reservation](actions/get-reservation.md) | GET |  |
| [List Reservations](actions/list-reservations.md) | GET |  |

### Routing Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Routing Form](actions/create-routing-form.md) | POST |  |
| [Get Routing Form](actions/get-routing-form.md) | GET |  |
| [List Routing Forms](actions/list-routing-forms.md) | GET |  |
| [Update Routing Form](actions/update-routing-form.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Schedule](actions/cancel-schedule.md) | PUT |  |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Get Schedule](actions/get-schedule.md) | GET |  |
| [List Recent Schedules](actions/list-recent-schedules.md) | GET |  |
| [Reschedule Schedule](actions/reschedule-schedule.md) | PUT |  |

### Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Slots](actions/list-calendar-slots.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Get Current Auth User](actions/get-current-auth-user.md) | GET |  |
| [Get My User](actions/get-my-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

