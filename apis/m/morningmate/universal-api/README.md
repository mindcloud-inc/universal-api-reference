# <img src="https://images.mindcloud.co/apps/icons/morningmate_1774966191500.png" alt="Morningmate logo" width="28" height="28"> Morningmate: Universal API

Manage projects, tasks, chat, and team workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/morningmate/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://morningmate.com
- **Vendor API docs:** https://api.morningmate.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Employees](actions/search-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Private Chat Room URL](actions/get-private-chat-room-url.md) | GET | Retrieves a private chat room URL from Morningmate. |
| [Invite Participants to Chat Room](actions/invite-participants-to-chat-room.md) | PUT | Invites participants to a Morningmate chat room. |

### Chat Room

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat Room](actions/get-chat-room.md) | GET | Retrieves a chat room from Morningmate by room ID. |
| [List Chat Rooms](actions/list-chat-rooms.md) | GET | Retrieves chat rooms for a Morningmate participant. |

### Division

| Action | Method | Description |
| --- | --- | --- |
| [List Divisions](actions/list-divisions.md) | GET | Retrieves divisions from Morningmate. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from Morningmate by user ID. |
| [Search Employees](actions/search-employees.md) | GET | Retrieves employees from Morningmate. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee v2](actions/get-employee-v2.md) | GET | Retrieves an employee from Morningmate's v2 API. |
| [List Employees v2](actions/list-employees-v2.md) | GET | Retrieves employees from Morningmate's v2 API. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message to Chat Room](actions/send-message-to-chat-room.md) | POST | Creates a message in a Morningmate chat room. |

### Notification Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET | Retrieves notification bots from Morningmate. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a post in a Morningmate project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Morningmate. |
| [Create Project Participants](actions/create-project-participants.md) | PUT | Adds participants to a Morningmate project. |
| [Search Participating Projects](actions/search-participating-projects.md) | GET | Retrieves Morningmate projects for a participant. |
| [Search Projects](actions/search-projects.md) | GET | Retrieves projects from Morningmate. |

### Project Participant

| Action | Method | Description |
| --- | --- | --- |
| [Search Project Participants](actions/search-project-participants.md) | GET | Retrieves participants for a Morningmate project. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Search SSO Participating Project](actions/search-sso-participating-project.md) | GET | Retrieves a Morningmate SSO project for a participant. |
| [Search SSO Participating Projects](actions/search-sso-participating-projects.md) | GET | Retrieves Morningmate SSO projects for a participant. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a schedule in a Morningmate project. |

### Sso Key

| Action | Method | Description |
| --- | --- | --- |
| [Generate RSA Public Key](actions/generate-rsa-public-key.md) | GET | Retrieves an RSA public key from Morningmate. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in a Morningmate project. |
| [Create Todo](actions/create-todo.md) | POST | Creates a todo in a Morningmate project. |
| [Update Task Status](actions/update-task-status.md) | PUT | Updates a task status in Morningmate. |

