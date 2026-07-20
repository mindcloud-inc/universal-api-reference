# <img src="https://images.mindcloud.co/apps/icons/ppfavicon_1774987399532.png" alt="Project Bubble logo" width="28" height="28"> Project Bubble: Universal API

Manage projects online with ProProfs Project for planning work, collaborating with teams, tracking time, and delivering projects on time.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/projectBubble/latest
- **Category:** Productivity / Project Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.proprofsproject.com/
- **Vendor API docs:** https://help.proprofsproject.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in a Project Bubble project. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Project Bubble. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Project Bubble by ID. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from Project Bubble. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Project Bubble. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Project Bubble. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a Project Bubble contact by ID. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Project Bubble. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Project Bubble. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Project Bubble. |
| [Get Event](actions/get-event.md) | GET | Retrieves a Project Bubble event by ID. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Project Bubble. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves project files from Project Bubble. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Project Bubble. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Project Bubble. |
| [Get Project](actions/get-project.md) | GET | Retrieves a Project Bubble project by ID. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Project Bubble. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in a Project Bubble project. |
| [Get Task](actions/get-task.md) | GET | Retrieves a Project Bubble task by ID. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Project Bubble. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a Project Bubble user by ID. |

