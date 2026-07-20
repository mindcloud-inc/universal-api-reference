# <img src="https://images.mindcloud.co/apps/icons/jitbit-helpdesk_1775508260175.png" alt="Jitbit Helpdesk logo" width="28" height="28"> Jitbit Helpdesk: Universal API

Jitbit Helpdesk provides ticketing, user, company, knowledge base, automation rule, and asset management APIs for support operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jitbitHelpdesk/latest
- **Category:** Support / Ticketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jitbit.com/helpdesk/
- **Vendor API docs:** https://www.jitbit.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Attachment](actions/get-attachment.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-attachment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET |  |
| [List Attachments](actions/list-attachments.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |

### Category Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields for Category](actions/list-custom-fields-for-category.md) | GET |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET |  |

### Comment Template

| Action | Method | Description |
| --- | --- | --- |
| [List Comment Templates](actions/list-comment-templates.md) | GET |  |

### Linked Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Tickets](actions/list-linked-tickets.md) | GET |  |

### Parent Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Get Parent Ticket](actions/get-parent-ticket.md) | GET |  |

### Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Priorities](actions/list-priorities.md) | GET |  |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats](actions/get-stats.md) | GET |  |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribers](actions/list-subscribers.md) | GET |  |

### Subticket

| Action | Method | Description |
| --- | --- | --- |
| [List Subtickets](actions/list-subtickets.md) | GET |  |

### Technician

| Action | Method | Description |
| --- | --- | --- |
| [List Techs for Category](actions/list-techs-for-category.md) | GET |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |

### Ticket Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Custom Fields](actions/list-ticket-custom-fields.md) | GET |  |

### Ticket Integration Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Integration Data](actions/get-ticket-integration-data.md) | GET |  |

### Ticket Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Tickets](actions/search-tickets.md) | GET |  |

### Time Spent Log

| Action | Method | Description |
| --- | --- | --- |
| [List Time Spent Log](actions/list-time-spent-log.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |

