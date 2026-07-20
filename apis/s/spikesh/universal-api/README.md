# <img src="https://images.mindcloud.co/apps/icons/ae1b268c-2c18-4f5e-85b6-b166a89b5865-2_1777311309919.png" alt="Spike.sh logo" width="28" height="28"> Spike.sh: Universal API

Incident management and on-call platform for alerts, escalations, services, and status pages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spikesh/latest
- **Category:** IT Operations / Observability
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spike.sh/
- **Vendor API docs:** https://docs.spike.sh/spike-api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Users](actions/get-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Alert Rules](actions/list-alert-rules.md) | GET | Retrieves alert rules for a team in Spike.sh. |

### Escalations

| Action | Method | Description |
| --- | --- | --- |
| [Get Escalation](actions/get-escalation.md) | GET | Retrieves escalation policy details from Spike.sh. |
| [List Escalations](actions/list-escalations.md) | GET | Retrieves all escalation policies from Spike.sh. |

### Incidents

| Action | Method | Description |
| --- | --- | --- |
| [List Acknowledged Incidents](actions/list-acknowledged-incidents.md) | GET | Retrieves acknowledged incidents for a team in Spike.sh. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves incidents for a team in Spike.sh. |
| [List Service Incidents](actions/list-service-incidents.md) | GET | Retrieves incidents for a service in Spike.sh. |
| [List Triggered Incidents](actions/list-triggered-incidents.md) | GET | Retrieves triggered incidents for a team in Spike.sh. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [List Available Integrations](actions/list-available-integrations.md) | GET | Retrieves all integrations available in Spike.sh. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations for a team in Spike.sh. |
| [List Service Integrations](actions/list-service-integrations.md) | GET | Retrieves integrations for a service in Spike.sh. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Info](actions/get-organization-info.md) | GET | Retrieves details for your Spike.sh organization. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Active On-Call Shifts](actions/list-active-on-call-shifts.md) | GET | Retrieves active on-call shifts from Spike.sh. |
| [List On-Calls](actions/list-on-calls.md) | GET | Retrieves on-call schedules for a team in Spike.sh. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in Spike.sh. |
| [Get Service](actions/get-service.md) | GET | Retrieves service details and incidents from Spike.sh. |
| [List Services](actions/list-services.md) | GET | Retrieves services for a team in Spike.sh. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in Spike.sh. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List All Teams](actions/list-all-teams.md) | GET | Retrieves all teams in your Spike.sh organization. |
| [List My Teams](actions/list-my-teams.md) | GET | Retrieves teams you belong to in Spike.sh. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves all users in your Spike.sh organization. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from your Spike.sh organization. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves all members in your Spike.sh organization. |

