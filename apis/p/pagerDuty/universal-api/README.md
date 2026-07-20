# <img src="https://images.mindcloud.co/apps/icons/pager-duty_1773431117808.png" alt="PagerDuty logo" width="28" height="28"> PagerDuty: Universal API

Manage incidents, services, schedules, teams, and on-call operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pagerDuty/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pagerduty.com
- **Vendor API docs:** https://developer.pagerduty.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Abilities](actions/list-abilities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-abilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Ability

| Action | Method | Description |
| --- | --- | --- |
| [List Abilities](actions/list-abilities.md) | GET |  |

### Escalation Policy

| Action | Method | Description |
| --- | --- | --- |
| [List Escalation Policies](actions/list-escalation-policies.md) | GET |  |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST |  |
| [List Incidents](actions/list-incidents.md) | GET |  |
| [Update Incident](actions/update-incident.md) | PUT |  |

### On-call

| Action | Method | Description |
| --- | --- | --- |
| [List On-Calls](actions/list-on-calls.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST |  |
| [Delete Service](actions/delete-service.md) | DELETE |  |
| [List Services](actions/list-services.md) | GET |  |
| [Update Service](actions/update-service.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

