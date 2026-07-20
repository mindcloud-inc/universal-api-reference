# <img src="https://images.mindcloud.co/apps/icons/proprofs-project-icon_1775570983603.png" alt="ProProfs Project logo" width="28" height="28"> ProProfs Project: Universal API

Access projects, tasks, subtasks, time entries, comments, files, events, clients, contacts, and webhook subscriptions in ProProfs Project through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proProfsProject/latest
- **Category:** Productivity / Project Management
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.proprofsproject.com/
- **Vendor API docs:** https://help.proprofsproject.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in ProProfs Project. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from ProProfs Project. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from ProProfs Project. |
| [List Clients](actions/list-clients.md) | GET | Retrieves a list of clients from ProProfs Project. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in ProProfs Project. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in ProProfs Project. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from ProProfs Project. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from ProProfs Project. |
| [List Comments](actions/list-comments.md) | GET | Retrieves a list of comments from ProProfs Project. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from ProProfs Project. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ProProfs Project. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from ProProfs Project. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from ProProfs Project. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from ProProfs Project. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ProProfs Project. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in ProProfs Project. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from ProProfs Project. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from ProProfs Project. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from ProProfs Project. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in ProProfs Project. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from ProProfs Project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in ProProfs Project. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from ProProfs Project. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from ProProfs Project. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from ProProfs Project. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in ProProfs Project. |

### Subtask

| Action | Method | Description |
| --- | --- | --- |
| [Create Subtask](actions/create-subtask.md) | POST | Creates a new subtask in ProProfs Project. |
| [Delete Subtask](actions/delete-subtask.md) | DELETE | Deletes an existing subtask from ProProfs Project. |
| [Get Subtask](actions/get-subtask.md) | GET | Retrieves a subtask from ProProfs Project. |
| [List Subtasks](actions/list-subtasks.md) | GET | Retrieves a list of subtasks from ProProfs Project. |
| [Update Subtask](actions/update-subtask.md) | PUT | Updates an existing subtask in ProProfs Project. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in ProProfs Project. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from ProProfs Project. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from ProProfs Project. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from ProProfs Project. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in ProProfs Project. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves a list of teams from ProProfs Project. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in ProProfs Project. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from ProProfs Project. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from ProProfs Project. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves a list of time entries from ProProfs Project. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in ProProfs Project. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from ProProfs Project. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from ProProfs Project. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in ProProfs Project. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from ProProfs Project. |

