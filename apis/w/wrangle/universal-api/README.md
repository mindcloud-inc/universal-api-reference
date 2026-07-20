# <img src="https://images.mindcloud.co/apps/icons/633465cd0ea37505173106fe-logo-1_1774300185577.png" alt="Wrangle logo" width="28" height="28"> Wrangle: Universal API

Manage Wrangle inboxes, tickets, and workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wrangle/latest
- **Category:** Support / Ticketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wrangle.io
- **Vendor API docs:** https://wrangle.apidocumentation.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Inboxes](actions/get-inboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox](actions/get-inbox.md) | GET |  |
| [Get Inboxes](actions/get-inboxes.md) | GET |  |
| [Update Inbox](actions/update-inbox.md) | PUT |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Delete Ticket](actions/delete-ticket.md) | DELETE |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [Get Tickets](actions/get-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [Get Workflows](actions/get-workflows.md) | GET |  |

### Workflow Instance

| Action | Method | Description |
| --- | --- | --- |
| [Start Workflow](actions/start-workflow.md) | POST |  |

