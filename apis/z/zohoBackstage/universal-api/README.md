# <img src="https://images.mindcloud.co/apps/icons/zoho-backstage_1773958706229.png" alt="Zoho Backstage logo" width="28" height="28"> Zoho Backstage: Universal API

Manage Zoho Backstage portals, events, members, speakers, agendas, sessions, attendees, orders, ticket classes, webhooks, and exhibitors through the official Zoho Backstage API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoBackstage/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://backstage.zoho.com/
- **Vendor API docs:** https://www.zoho.com/backstage/api/v3/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Portals](actions/list-portals.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [List Attendees](actions/list-attendees.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Exhibitors](actions/list-exhibitors.md) | GET |  |
| [List Sponsors](actions/list-sponsors.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Delete Event](actions/delete-event.md) | DELETE |  |
| [List Events](actions/list-events.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Agenda](actions/create-agenda.md) | POST |  |
| [List Agendas](actions/list-agendas.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [List Sessions](actions/list-sessions.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Classes](actions/list-ticket-classes.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Speaker](actions/create-speaker.md) | POST |  |
| [List Event Members](actions/list-event-members.md) | GET |  |
| [List Portal Members](actions/list-portal-members.md) | GET |  |
| [List Speakers](actions/list-speakers.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Webhook](actions/create-event-webhook.md) | POST |  |
| [Create Portal Webhook](actions/create-portal-webhook.md) | POST |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Portals](actions/list-portals.md) | GET |  |

