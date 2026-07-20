# <img src="https://images.mindcloud.co/apps/icons/team-book_1775668709040.png" alt="TeamBook logo" width="28" height="28"> TeamBook: Universal API

TeamBook is a resource planning and scheduling platform for projects, teams, bookings, clients, tasks, capacity tracking, and actual logs. This wrapper targets TeamBook's public REST API and currently focuses on the provable public surface around projects, users, bookings, clients, teams, tasks, and actual logs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamBook/latest
- **Category:** Productivity / Project Management
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://web.teambookapp.com
- **Vendor API docs:** https://kb.teambookapp.com/en/article/teambook-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Actual Log

| Action | Method | Description |
| --- | --- | --- |
| [Create Actual Logs](actions/create-actual-logs.md) | POST | Creates new actual logs in TeamBook. |
| [List Actual Logs](actions/list-actual-logs.md) | GET | Retrieves actual log records from TeamBook. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in TeamBook. |
| [Delete Booking](actions/delete-booking.md) | DELETE | Deletes an existing booking from TeamBook. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves detailed booking information from TeamBook. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves all booking records from TeamBook. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in TeamBook. |
| [Get Client](actions/get-client.md) | GET | Retrieves detailed client information from TeamBook. |
| [List Clients](actions/list-clients.md) | GET | Retrieves all client records from TeamBook. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in TeamBook. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from TeamBook. |
| [Get Project](actions/get-project.md) | GET | Retrieves detailed project information from TeamBook. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from TeamBook. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in TeamBook. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from TeamBook. |
| [Get Task](actions/get-task.md) | GET | Retrieves detailed task information from TeamBook. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from TeamBook. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves detailed team information from TeamBook. |
| [List Teams](actions/list-teams.md) | GET | Retrieves all team records from TeamBook. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in TeamBook. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from TeamBook. |
| [Get User](actions/get-user.md) | GET | Retrieves detailed user information from TeamBook. |
| [List Users](actions/list-users.md) | GET | Retrieves all user records from TeamBook. |

