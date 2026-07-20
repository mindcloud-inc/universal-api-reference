# <img src="https://images.mindcloud.co/apps/icons/teamgate_1774640194387.png" alt="Teamgate logo" width="28" height="28"> Teamgate: Universal API

Manage leads, people, companies, deals, and activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamgate/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.teamgate.com
- **Vendor API docs:** https://developers.teamgate.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Teamgate. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an activity in Teamgate. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Teamgate. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Teamgate. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a new call in Teamgate. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Teamgate. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes a company from Teamgate. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Teamgate. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Teamgate. |
| [List Deal Companies](actions/list-deal-companies.md) | GET | Retrieves companies for a deal in Teamgate. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Teamgate. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in Teamgate. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Teamgate. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes a deal from Teamgate. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Teamgate. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from Teamgate. |
| [List Person Deals](actions/list-person-deals.md) | GET | Retrieves deals for a person in Teamgate. |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in Teamgate. |
| [Update Deal](actions/update-deal.md) | PUT | Updates a deal in Teamgate. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Teamgate. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes a lead from Teamgate. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Teamgate. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Teamgate. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in Teamgate. |
| [Update Lead](actions/update-lead.md) | PUT | Updates a lead in Teamgate. |

### Lead Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Activities](actions/list-lead-activities.md) | GET | Retrieves activities for a lead in Teamgate. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Teamgate. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Teamgate. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes a person from Teamgate. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Teamgate. |
| [List Deal People](actions/list-deal-people.md) | GET | Retrieves people for a deal in Teamgate. |
| [List People](actions/list-people.md) | GET | Retrieves people from Teamgate. |
| [Search People](actions/search-people.md) | GET | Finds people in Teamgate. |
| [Update Person](actions/update-person.md) | PUT | Updates a person in Teamgate. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Statuses](actions/list-lead-statuses.md) | GET | Retrieves lead statuses from Teamgate. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Teamgate. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Teamgate. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Teamgate. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from Teamgate. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Teamgate. |

