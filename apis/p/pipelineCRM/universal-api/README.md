# <img src="https://images.mindcloud.co/apps/icons/pipeline-crm_1773855615985.png" alt="Pipeline CRM logo" width="28" height="28"> Pipeline CRM: Universal API

Manage Pipeline CRM deals, people, companies, tasks, and activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipelineCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.pipelinecrm.com
- **Vendor API docs:** https://app.pipelinecrm.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Activities](actions/list-activities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity note in Pipeline CRM. |
| [List Activities](actions/list-activities.md) | GET | Finds activity notes in Pipeline CRM for a deal, person, or company. |
| [Retrieve Activity](actions/retrieve-activity.md) | GET | Retrieves an activity note from Pipeline CRM. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity note in Pipeline CRM. |

### Calendar Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Entry](actions/create-calendar-entry.md) | POST | Creates a new calendar task or event in Pipeline CRM. |
| [Delete Calendar Entry](actions/delete-calendar-entry.md) | DELETE | Deletes an existing calendar entry from Pipeline CRM. |
| [List Calendar Entries](actions/list-calendar-entries.md) | GET | Finds calendar entries in Pipeline CRM. |
| [Retrieve Calendar Entry](actions/retrieve-calendar-entry.md) | GET | Retrieves a calendar entry from Pipeline CRM. |
| [Update Calendar Entry](actions/update-calendar-entry.md) | PUT | Updates an existing calendar entry in Pipeline CRM. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Pipeline CRM. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Pipeline CRM. |
| [List Companies](actions/list-companies.md) | GET | Finds companies in Pipeline CRM. |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves a company from Pipeline CRM. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Pipeline CRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Pipeline CRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Pipeline CRM. |
| [List Deals](actions/list-deals.md) | GET | Finds deals in Pipeline CRM. |
| [Retrieve Deal](actions/retrieve-deal.md) | GET | Retrieves a deal from Pipeline CRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Pipeline CRM. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Pipeline CRM. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from Pipeline CRM. |
| [List People](actions/list-people.md) | GET | Finds people in Pipeline CRM. |
| [Retrieve Person](actions/retrieve-person.md) | GET | Retrieves a person from Pipeline CRM. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Pipeline CRM. |

