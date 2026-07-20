# <img src="https://images.mindcloud.co/apps/icons/manus_1773759431396.png" alt="Manus logo" width="28" height="28"> Manus: Universal API

Create and manage Manus projects, tasks, files, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/manus/latest
- **Category:** Productivity / Project Management
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://manus.im
- **Vendor API docs:** https://open.manus.ai/docs/v1/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manus/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a file in Manus and returns a presigned upload URL. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Manus and its stored content. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Manus by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves the 10 most recently uploaded files from Manus. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Manus. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Manus. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Manus. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from Manus. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Manus by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Manus with optional filtering and pagination. |
| [Update Task](actions/update-task.md) | PUT | Updates task metadata in Manus. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Manus. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Manus. |

