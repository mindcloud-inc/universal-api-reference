# <img src="https://images.mindcloud.co/apps/icons/central-station-crm_1775166266543.png" alt="CentralStationCRM logo" width="28" height="28"> CentralStationCRM: Universal API

Manage contacts, deals, tasks, and team sales work

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/centralStationCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://centralstationcrm.com
- **Vendor API docs:** https://api.centralstationcrm.net/api-docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Connection](actions/check-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in CentralStationCRM. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from CentralStationCRM. |
| [Get Company](actions/get-company.md) | GET | Retrieves a single company from CentralStationCRM. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all available companies from CentralStationCRM. |
| [Merge Companies](actions/merge-companies.md) | PUT | Merges duplicate company records in CentralStationCRM. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in CentralStationCRM by search term. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in CentralStationCRM. |

### Company Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Companies](actions/count-companies.md) | GET | Retrieves the companies count from CentralStationCRM. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | GET | Checks the current CentralStationCRM API connection. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in CentralStationCRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a single deal from CentralStationCRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves all available deals from CentralStationCRM. |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in CentralStationCRM by search term. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in CentralStationCRM. |

### Deal Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Deals](actions/count-deals.md) | GET | Retrieves the deals count from CentralStationCRM. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in CentralStationCRM. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from CentralStationCRM. |
| [Get Person](actions/get-person.md) | GET | Retrieves a single person from CentralStationCRM. |
| [List People](actions/list-people.md) | GET | Retrieves all available people from CentralStationCRM. |
| [Merge People](actions/merge-people.md) | PUT | Merges duplicate people records in CentralStationCRM. |
| [Search People](actions/search-people.md) | GET | Finds people in CentralStationCRM by search term. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in CentralStationCRM. |

### Person Count

| Action | Method | Description |
| --- | --- | --- |
| [Count People](actions/count-people.md) | GET | Retrieves the people count from CentralStationCRM. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in CentralStationCRM. |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project from CentralStationCRM. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all available projects from CentralStationCRM. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in CentralStationCRM. |

### Protocol

| Action | Method | Description |
| --- | --- | --- |
| [Create Protocol](actions/create-protocol.md) | POST | Creates a new protocol in CentralStationCRM. |
| [Get Protocol](actions/get-protocol.md) | GET | Retrieves a single protocol from CentralStationCRM. |
| [List Protocols](actions/list-protocols.md) | GET | Retrieves all available protocols from CentralStationCRM. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Records](actions/search-records.md) | GET | Finds matching records in CentralStationCRM by search term. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in CentralStationCRM. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from CentralStationCRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves a single task from CentralStationCRM. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all available tasks from CentralStationCRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in CentralStationCRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from CentralStationCRM. |
| [Get User](actions/get-user.md) | GET | Retrieves a single user from CentralStationCRM. |
| [List Users](actions/list-users.md) | GET | Retrieves all available users from CentralStationCRM. |
| [Search Users](actions/search-users.md) | GET | Finds users in CentralStationCRM by search term. |

