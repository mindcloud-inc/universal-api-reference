# <img src="https://images.mindcloud.co/apps/icons/timewax_1776742369255.png" alt="Timewax logo" width="28" height="28"> Timewax: Universal API

Timewax is resource planning software for service organizations, with APIs for project planning, resources, clients, planning bookings, time sheets, progress, and Gantt chart data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timewax/latest
- **Category:** Productivity / Scheduling
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.timewax.com/
- **Vendor API docs:** https://timewax.atlassian.net/servicedesk/customer/portal/7/topic/a7c3f08f-024f-4dc1-9484-a92c06be3724

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authentication Token](actions/get-authentication-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Authentication Token](actions/get-authentication-token.md) | GET | Retrieves an authentication token from Timewax. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Timewax. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Timewax. |
| [List Clients](actions/list-clients.md) | GET | Retrieves all clients from Timewax. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Timewax. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST | Creates a new department in Timewax. |
| [Get Department](actions/get-department.md) | GET | Retrieves a department from Timewax. |
| [List Departments](actions/list-departments.md) | GET | Retrieves all departments from Timewax. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in Timewax. |

### Planning Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Planning Booking](actions/create-planning-booking.md) | POST | Creates a new planning booking in Timewax. |
| [List Changed Planning Bookings](actions/list-changed-planning-bookings.md) | GET | Retrieves changed planning bookings from Timewax by date range. |
| [List Planning Bookings](actions/list-planning-bookings.md) | GET | Retrieves planning booking records from Timewax. |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | POST | Creates a new position in Timewax. |
| [Update Position](actions/update-position.md) | PUT | Updates an existing position in Timewax. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Timewax. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Timewax. |
| [List Changed Projects](actions/list-changed-projects.md) | GET | Retrieves changed projects from Timewax by date range. |
| [List Inactive Projects](actions/list-inactive-projects.md) | GET | Retrieves all inactive projects from Timewax. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all projects from Timewax. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Timewax. |

### Project Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Activity](actions/create-project-activity.md) | POST | Creates a new project activity in Timewax. |
| [Get Project Activity](actions/get-project-activity.md) | GET | Retrieves a project activity from Timewax. |
| [List Project Activities](actions/list-project-activities.md) | GET | Retrieves all project activities from Timewax. |
| [Update Project Activity](actions/update-project-activity.md) | PUT | Updates an existing project activity in Timewax. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Timewax. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Timewax. |
| [List Resources](actions/list-resources.md) | GET | Retrieves all resource records from Timewax. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Timewax. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Timewax. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entry records from Timewax. |

