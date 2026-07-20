# <img src="https://images.mindcloud.co/apps/icons/id-d1xuk-c6n-logos_1777047784863.jpeg" alt="NeetoDesk logo" width="28" height="28"> NeetoDesk: Universal API

Manage NeetoDesk tickets, comments, reports, and team members

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neetoDesk/latest
- **Category:** Support / Ticketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.neeto.com/neetodesk
- **Vendor API docs:** https://apidocs.neetodesk.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Team Members](actions/list-team-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Agent Performance Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Performance Report](actions/get-agent-performance-report.md) | GET |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Get Comment](actions/get-comment.md) | GET |  |
| [List Comments](actions/list-comments.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |

### Customer Satisfaction Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Satisfaction Report](actions/get-customer-satisfaction-report.md) | GET |  |

### Draft Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Comment](actions/create-draft-comment.md) | POST |  |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | POST |  |
| [Get Team Member Details](actions/get-team-member-details.md) | GET |  |
| [List Team Members](actions/list-team-members.md) | GET |  |
| [Remove Team Member](actions/remove-team-member.md) | DELETE |  |
| [Update Team Member](actions/update-team-member.md) | PUT |  |

### Team Performance Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Performance Report](actions/get-team-performance-report.md) | GET |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

### Ticket Volume Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Volume Report](actions/get-ticket-volume-report.md) | GET |  |

### Ticket Volume Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Volume Time Series](actions/get-ticket-volume-time-series.md) | GET |  |

