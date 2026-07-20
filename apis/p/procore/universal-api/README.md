# <img src="https://images.mindcloud.co/apps/icons/procore_1774285479669.png" alt="Procore logo" width="28" height="28"> Procore: Universal API

Manage construction projects, resources, and financials

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/procore/latest
- **Category:** Productivity / Project Management
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.procore.com
- **Vendor API docs:** https://developers.procore.com/reference/rest/docs/rest-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/procore/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [Get Budget Metadata](actions/get-budget-metadata.md) | GET | Retrieves budget metadata from Procore. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Procore. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Procore. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in Procore. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves incidents from Procore. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Action Plan](actions/create-action-plan.md) | POST | Creates a new action plan in Procore. |
| [Create Change Event](actions/create-change-event.md) | POST | Creates a new change event in Procore. |
| [List Action Plans](actions/list-action-plans.md) | GET | Retrieves action plans from Procore. |
| [List Change Events](actions/list-change-events.md) | GET | Retrieves change events from Procore. |
| [List Commitment Contracts](actions/list-commitment-contracts.md) | GET | Retrieves commitment contracts from Procore. |
| [List Drawing Areas](actions/list-drawing-areas.md) | GET | Retrieves drawing areas from Procore. |
| [List Drawings](actions/list-drawings.md) | GET | Retrieves drawings from Procore. |
| [List Observations](actions/list-observations.md) | GET | Retrieves observation items from Procore. |
| [List Project Documents](actions/list-project-documents.md) | GET | Retrieves project folders and files from Procore. |
| [List Project Locations](actions/list-project-locations.md) | GET | Retrieves project locations from Procore. |
| [List Schedule Activities](actions/list-schedule-activities.md) | GET | Retrieves schedule activities from Procore. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Procore. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule Metadata](actions/get-schedule-metadata.md) | GET | Retrieves schedule metadata from Procore. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Procore. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from Procore. |
| [Update Timesheet Status](actions/update-timesheet-status.md) | PUT | Updates a timesheet approval status in Procore. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Procore. |
| [List Company Users](actions/list-company-users.md) | GET | Retrieves company users from Procore. |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves project users from Procore. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [List Company Vendors](actions/list-company-vendors.md) | GET | Retrieves company vendors from Procore. |
| [List Project Vendors](actions/list-project-vendors.md) | GET | Retrieves project vendors from Procore. |

