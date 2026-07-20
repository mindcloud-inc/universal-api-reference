# <img src="https://images.mindcloud.co/apps/icons/timetoreply_1775667859088.png" alt="Timetoreply logo" width="28" height="28"> Timetoreply: Universal API

Track, analyze, and improve team email response performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timetoreply/latest
- **Category:** Support / Ticketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timetoreply.com/
- **Vendor API docs:** https://portal.timetoreply.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Alerts](actions/list-agent-alerts.md) | GET |  |
| [List Alerts](actions/list-alerts.md) | GET |  |

### Comparative Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Comparative Report](actions/get-comparative-report.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Contact Group

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Groups](actions/list-contact-groups.md) | GET |  |

### Contacts Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Contacts Report](actions/get-contacts-report.md) | GET |  |

### Conversation Log

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Logs](actions/list-conversation-logs.md) | GET |  |

### Group Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [List Group Mailboxes](actions/list-group-mailboxes.md) | GET |  |

### Group Mailboxes Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Mailboxes Report](actions/get-group-mailboxes-report.md) | GET |  |

### Interactions Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Interactions Report](actions/get-interactions-report.md) | GET |  |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [List Mailboxes](actions/list-mailboxes.md) | GET |  |

### Message Log

| Action | Method | Description |
| --- | --- | --- |
| [List Message Logs](actions/list-message-logs.md) | GET |  |

### Overview Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Overview Report](actions/get-overview-report.md) | GET |  |

### Productivity Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Productivity Report](actions/get-productivity-report.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET |  |

### Sla Report

| Action | Method | Description |
| --- | --- | --- |
| [Get SLA Report](actions/get-sla-report.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### Teams Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Teams Report](actions/get-teams-report.md) | GET |  |

### Trend Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Trend Report](actions/get-trend-report.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

