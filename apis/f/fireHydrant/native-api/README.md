# FireHydrant: Native API Reference

A consolidated summary of FireHydrant's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.firehydrant.com/reference/introduction-to-the-firehydrant-api
- **API base URL:** `https://api.firehydrant.io/v1`

## Authentication

### API Key

Use a FireHydrant API key with the raw token value sent in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.firehydrant.com/docs/api-keys)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Incident](actions/archive-incident.md) | `DELETE /incidents/:incident_id` | [docs](https://docs.firehydrant.com/reference/delete_incident) |
| [Create Incident](actions/create-incident.md) | `POST /incidents` | [docs](https://docs.firehydrant.com/reference/create_incident) |
| [Create Incident Note](actions/create-incident-note.md) | `POST /incidents/:incident_id/notes` | [docs](https://docs.firehydrant.com/reference/create_incident_note) |
| [Create Incident Task](actions/create-incident-task.md) | `POST /incidents/:incident_id/tasks` | [docs](https://docs.firehydrant.com/reference/create_incident_task) |
| [Get Environment](actions/get-environment.md) | `GET /environments/:environment_id` | [docs](https://docs.firehydrant.com/reference/get_environment) |
| [Get Incident](actions/get-incident.md) | `GET /incidents/:incident_id` | [docs](https://docs.firehydrant.com/reference/get_incident) |
| [Get Service](actions/get-service.md) | `GET /services/:service_id` | [docs](https://docs.firehydrant.com/reference/get_service) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://docs.firehydrant.com/reference/list_environments) |
| [List Functionalities](actions/list-functionalities.md) | `GET /functionalities` | [docs](https://docs.firehydrant.com/reference/list_functionalities) |
| [List Incident Assignees](actions/list-incident-assignees.md) | `GET /incidents/:incident_id/role_assignments` | [docs](https://docs.firehydrant.com/reference/list_incident_role_assignments) |
| [List Incident Events](actions/list-incident-events.md) | `GET /incidents/:incident_id/events` | [docs](https://docs.firehydrant.com/reference/list_incident_events) |
| [List Incident Impacts](actions/list-incident-impacts.md) | `GET /incidents/:incident_id/impact/:type` | [docs](https://docs.firehydrant.com/reference/list_incident_impacts) |
| [List Incident Roles](actions/list-incident-roles.md) | `GET /incident_roles` | [docs](https://docs.firehydrant.com/reference/list_incident_roles) |
| [List Incident Tasks](actions/list-incident-tasks.md) | `GET /incidents/:incident_id/tasks` | [docs](https://docs.firehydrant.com/reference/list_incident_tasks) |
| [List Incident Types](actions/list-incident-types.md) | `GET /incident_types` | [docs](https://docs.firehydrant.com/reference/list_incident_types) |
| [List Incidents](actions/list-incidents.md) | `GET /incidents` | [docs](https://docs.firehydrant.com/reference/list_incidents) |
| [List Priorities](actions/list-priorities.md) | `GET /priorities` | [docs](https://docs.firehydrant.com/reference/list_priorities) |
| [List Runbooks](actions/list-runbooks.md) | `GET /runbooks` | [docs](https://docs.firehydrant.com/reference/list_runbooks) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://docs.firehydrant.com/reference/list_services) |
| [List Severities](actions/list-severities.md) | `GET /severities` | [docs](https://docs.firehydrant.com/reference/list_severities) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.firehydrant.com/reference/list_teams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.firehydrant.com/reference/list_users) |
| [Update Incident](actions/update-incident.md) | `PATCH /incidents/:incident_id` | [docs](https://docs.firehydrant.com/reference/update_incident) |
| [Update Incident Task](actions/update-incident-task.md) | `PATCH /incidents/:incident_id/tasks/:task_id` | [docs](https://docs.firehydrant.com/reference/update_incident_task) |
