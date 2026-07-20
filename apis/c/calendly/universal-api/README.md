# <img src="https://images.mindcloud.co/apps/icons/calendly-icon_1772136126114.png" alt="Calendly logo" width="28" height="28"> Calendly: Universal API

Schedule meetings, share booking links, automate reminders, and route invitees.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calendly/latest
- **Category:** Marketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.calendly.com/api-docs/4b402d5ab3edd-calendly-developer
- **Vendor API docs:** https://developer.calendly.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Event Type Available Times](actions/list-event-type-available-times.md) | GET | Retrieves available times for a Calendly event type. |
| [List User Availability Schedules](actions/list-user-availability-schedules.md) | GET | Retrieves user availability schedules from Calendly. |
| [List User Busy Times](actions/list-user-busy-times.md) | GET | Retrieves user busy times from Calendly. |

### Event Invitee

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Invitee](actions/create-event-invitee.md) | POST | Creates an event invitee in Calendly. |

### Event Invitees

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Invitee](actions/get-event-invitee.md) | GET | Retrieves an invitee for a Calendly event. |
| [List Event Invitees](actions/list-event-invitees.md) | GET | Retrieves invitees for a Calendly event. |

### Event Types

| Action | Method | Description |
| --- | --- | --- |
| [Create One-Off Event Type](actions/create-one-off-event-type.md) | POST | Creates a one-off event type in Calendly. |
| [Get Event Type](actions/get-event-type.md) | GET | Retrieves an event type from Calendly. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types from Calendly. |

### Invitee No Shows

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitee No Show](actions/create-invitee-no-show.md) | POST | Marks an invitee as a no-show in Calendly. |
| [Get Invitee No Show](actions/get-invitee-no-show.md) | GET | Retrieves an invitee no-show from Calendly. |
| [Unmark Invitee No Show](actions/unmark-invitee-no-show.md) | DELETE | Removes a no-show mark from a Calendly invitee. |

### Organization Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Memberships](actions/list-organization-memberships.md) | GET | Retrieves organization memberships from Calendly. |

### Routing Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Routing Form Submissions](actions/list-routing-form-submissions.md) | GET | Retrieves routing form submissions from Calendly. |
| [Submit Routing Form](actions/submit-routing-form.md) | POST | Submits a routing form in Calendly. |

### Routing Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Routing Form](actions/get-routing-form.md) | GET | Retrieves a routing form from Calendly. |
| [List Routing Forms](actions/list-routing-forms.md) | GET | Retrieves routing forms from Calendly. |

### Scheduled Events

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | POST | Cancels a scheduled event in Calendly. |
| [Get Scheduled Event](actions/get-scheduled-event.md) | GET | Retrieves a scheduled event from Calendly. |
| [List Scheduled Events](actions/list-scheduled-events.md) | GET | Retrieves scheduled events from Calendly. |

### Scheduling Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Single-Use Scheduling Link](actions/create-single-use-scheduling-link.md) | POST | Creates a single-use scheduling link in Calendly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Calendly. |

### Webhook Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Calendly. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from Calendly. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from Calendly. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from Calendly. |

