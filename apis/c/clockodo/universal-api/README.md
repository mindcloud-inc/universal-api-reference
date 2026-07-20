# <img src="https://images.mindcloud.co/apps/icons/images-2_1774553554488.png" alt="Clockodo logo" width="28" height="28"> Clockodo: Universal API

Clockodo time tracking and work-time API wrapper.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clockodo/latest
- **Category:** Human Resources / HRIS
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clockodo.com/
- **Vendor API docs:** https://www.clockodo.com/en/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Services](actions/list-services.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Clock

| Action | Method | Description |
| --- | --- | --- |
| [Change Duration](actions/change-duration.md) | PUT | Updates the clock duration in your Clockodo account. |
| [Get Currently Running Entries](actions/get-currently-running-entries.md) | GET | Retrieves currently running entries from your Clockodo account. |
| [Start Clock](actions/start-clock.md) | POST | Starts the clock in your Clockodo account. |
| [Stop Clock](actions/stop-clock.md) | DELETE | Stops the clock in your Clockodo account. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in your Clockodo account. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes a customer from your Clockodo account. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from your Clockodo account. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from your Clockodo account. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in your Clockodo account. |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST | Creates a time entry in your Clockodo account. |
| [Delete Entry](actions/delete-entry.md) | DELETE | Deletes a time entry from your Clockodo account. |
| [Get Entry](actions/get-entry.md) | GET | Retrieves a time entry from your Clockodo account. |
| [List Entries](actions/list-entries.md) | GET | Retrieves time entries from your Clockodo account. |
| [Update Entry](actions/update-entry.md) | PUT | Updates a time entry in your Clockodo account. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in your Clockodo account. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from your Clockodo account. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your Clockodo account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Clockodo account. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in your Clockodo account. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a service in your Clockodo account. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes a service from your Clockodo account. |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from your Clockodo account. |
| [List Services](actions/list-services.md) | GET | Retrieves services from your Clockodo account. |
| [Update Service](actions/update-service.md) | PUT | Updates a service in your Clockodo account. |

