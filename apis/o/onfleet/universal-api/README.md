# <img src="https://images.mindcloud.co/apps/icons/onfleet_1773935135302.png" alt="Onfleet logo" width="28" height="28"> Onfleet: Universal API

Manage drivers, teams, tasks, and deliveries with Onfleet

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onfleet/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onfleet.com
- **Vendor API docs:** https://docs.onfleet.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key](actions/test-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key](actions/test-api-key.md) | GET | Tests an Onfleet API key for validity. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [Create Destination](actions/create-destination.md) | POST | Creates a new destination in Onfleet. |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from Onfleet. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves your organization's details from Onfleet. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in Onfleet. |
| [Find Recipient](actions/find-recipient.md) | GET | Finds a recipient in Onfleet by name or phone. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves a recipient from Onfleet. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in Onfleet. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Assign Tasks](actions/auto-assign-tasks.md) | PUT | Assigns tasks to workers automatically in Onfleet. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Onfleet. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Onfleet. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Onfleet. |
| [List Team Tasks](actions/list-team-tasks.md) | GET | Retrieves unassigned tasks for a team in Onfleet. |
| [List Worker Tasks](actions/list-worker-tasks.md) | GET | Retrieves tasks assigned to a worker in Onfleet. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Onfleet. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Onfleet. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Onfleet. |
| [List Teams](actions/list-teams.md) | GET | Retrieves a list of teams from Onfleet. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in Onfleet. |

### Worker

| Action | Method | Description |
| --- | --- | --- |
| [Create Worker](actions/create-worker.md) | POST | Creates a new worker in Onfleet. |
| [Get Worker](actions/get-worker.md) | GET | Retrieves a worker from Onfleet. |
| [Get Workers By Location](actions/get-workers-by-location.md) | GET | Finds workers in Onfleet near a location. |
| [List Workers](actions/list-workers.md) | GET | Retrieves a list of workers from Onfleet. |
| [Update Worker](actions/update-worker.md) | PUT | Updates an existing worker in Onfleet. |

