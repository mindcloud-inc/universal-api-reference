# <img src="https://images.mindcloud.co/apps/icons/fire-hydrant_1776981308987.png" alt="FireHydrant logo" width="28" height="28"> FireHydrant: Universal API

FireHydrant is an alerting and incident management platform for declaring incidents, coordinating responders, automating response work, and reviewing reliability events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fireHydrant/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://firehydrant.com
- **Vendor API docs:** https://docs.firehydrant.com/reference/introduction-to-the-firehydrant-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Environments](actions/list-environments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an environment from FireHydrant. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from FireHydrant. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Events](actions/list-incident-events.md) | GET | Retrieves incident events from FireHydrant. |

### Functionality

| Action | Method | Description |
| --- | --- | --- |
| [List Functionalities](actions/list-functionalities.md) | GET | Retrieves all functionality records from FireHydrant. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Archive Incident](actions/archive-incident.md) | DELETE | Archives an existing incident in FireHydrant. |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in FireHydrant. |
| [Get Incident](actions/get-incident.md) | GET | Retrieves an incident from FireHydrant. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves incidents from FireHydrant. |
| [Update Incident](actions/update-incident.md) | PUT | Updates an existing incident in FireHydrant. |

### Incident Impact

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Impacts](actions/list-incident-impacts.md) | GET | Retrieves incident impacts by type from FireHydrant. |

### Incident Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident Note](actions/create-incident-note.md) | POST | Creates a new incident note in FireHydrant. |

### Incident Role

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Roles](actions/list-incident-roles.md) | GET | Retrieves incident roles from FireHydrant. |

### Incident Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident Task](actions/create-incident-task.md) | POST | Creates a new incident task in FireHydrant. |
| [List Incident Tasks](actions/list-incident-tasks.md) | GET | Retrieves incident tasks from FireHydrant. |
| [Update Incident Task](actions/update-incident-task.md) | PUT | Updates an existing incident task in FireHydrant. |

### Incident Type

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Types](actions/list-incident-types.md) | GET | Retrieves incident types from FireHydrant. |

### Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves incident priorities from FireHydrant. |

### Role Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Assignees](actions/list-incident-assignees.md) | GET | Retrieves incident role assignments from FireHydrant. |

### Runbook

| Action | Method | Description |
| --- | --- | --- |
| [List Runbooks](actions/list-runbooks.md) | GET | Retrieves runbooks from FireHydrant. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from FireHydrant. |
| [List Services](actions/list-services.md) | GET | Retrieves services from FireHydrant. |

### Severity

| Action | Method | Description |
| --- | --- | --- |
| [List Severities](actions/list-severities.md) | GET | Retrieves incident severities from FireHydrant. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from FireHydrant. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from FireHydrant. |

