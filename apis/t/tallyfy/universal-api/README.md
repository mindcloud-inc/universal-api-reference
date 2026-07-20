# <img src="https://images.mindcloud.co/apps/icons/tallyfy_1774277527141.png" alt="Tallyfy logo" width="28" height="28"> Tallyfy: Universal API

Tallyfy is an API-first workflow automation platform for managing templates, processes, tasks, guests, and related workflow operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tallyfy/latest
- **Category:** Productivity / Project Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tallyfy.com
- **Vendor API docs:** https://tallyfy.com/products/pro/integrations/open-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Member](actions/get-current-member.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Checklist

| Action | Method | Description |
| --- | --- | --- |
| [List Checklists](actions/list-checklists.md) | GET | Retrieves checklist blueprints from your Tallyfy organization. |

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Tallyfy. |
| [Create Template With Steps](actions/create-template-with-steps.md) | POST | Creates a new template with steps in Tallyfy. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Tallyfy. |
| [List Templates](actions/list-templates.md) | GET | Retrieves process templates from your Tallyfy organization. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Tallyfy. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from your Tallyfy organization. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks across your Tallyfy organization. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Complete Process Task](actions/complete-process-task.md) | PUT | Completes a process task in Tallyfy. |
| [Create Task](actions/create-task.md) | POST | Creates a new one-off task in Tallyfy. |
| [Get Process Task](actions/get-process-task.md) | GET | Retrieves a process task from Tallyfy. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Tallyfy. |
| [List Process Tasks](actions/list-process-tasks.md) | GET | Retrieves tasks for a process in Tallyfy. |
| [Reopen Process Task](actions/reopen-process-task.md) | PUT | Reopens a completed process task in Tallyfy. |
| [Search Tasks](actions/search-tasks.md) | GET | Finds tasks in Tallyfy by search criteria. |
| [Update Process Task](actions/update-process-task.md) | PUT | Updates an existing process task in Tallyfy. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Tallyfy. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Member](actions/get-current-member.md) | GET | Retrieves the current member from Tallyfy. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Tallyfy organization. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Guest](actions/create-guest.md) | POST | Creates a new guest in Tallyfy. |
| [List Guests](actions/list-guests.md) | GET | Retrieves guests from your Tallyfy organization. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Create Process](actions/create-process.md) | POST | Creates a new process from a template in Tallyfy. |
| [Get Process](actions/get-process.md) | GET | Retrieves a process from Tallyfy. |
| [List Processes](actions/list-processes.md) | GET | Retrieves processes from your Tallyfy organization. |
| [Update Process](actions/update-process.md) | PUT | Updates an existing process in Tallyfy. |

