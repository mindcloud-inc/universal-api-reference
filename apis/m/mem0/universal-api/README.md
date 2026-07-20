# <img src="https://images.mindcloud.co/apps/icons/mem0-logo_1776095534053.jpeg" alt="Mem0 logo" width="28" height="28"> Mem0: Universal API

Memory layer for AI agents and applications, with APIs for storing, searching, updating, exporting, and managing user-scoped memories, organizations, projects, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mem0/latest
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mem0.ai
- **Vendor API docs:** https://docs.mem0.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Delete Entity](actions/delete-entity.md) | DELETE | Deletes an entity from Mem0. |
| [List Entities](actions/list-entities.md) | GET | Retrieves entities from Mem0. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Mem0. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Mem0. |

### Memory

| Action | Method | Description |
| --- | --- | --- |
| [Add Memories](actions/add-memories.md) | POST |  |
| [Batch Delete Memories](actions/batch-delete-memories.md) | DELETE | Deletes multiple memories from Mem0. |
| [Batch Update Memories](actions/batch-update-memories.md) | PUT | Updates multiple memories in Mem0. |
| [Delete Memories](actions/delete-memories.md) | DELETE | Deletes memories from Mem0 by scope or filter. |
| [Delete Memory](actions/delete-memory.md) | DELETE | Deletes an existing memory from Mem0. |
| [Get Memory](actions/get-memory.md) | GET | Retrieves a memory from Mem0. |
| [List Memories](actions/list-memories.md) | GET |  |
| [Search Memories](actions/search-memories.md) | GET |  |
| [Update Memory](actions/update-memory.md) | PUT | Updates an existing memory in Mem0. |

### Memory Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Memory Export](actions/create-memory-export.md) | POST | Creates a new memory export job in Mem0. |
| [Get Memory Export](actions/get-memory-export.md) | GET | Retrieves a memory export from Mem0. |

### Memory Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Submit Memory Feedback](actions/submit-memory-feedback.md) | POST | Submits feedback for a memory in Mem0. |

### Memory History

| Action | Method | Description |
| --- | --- | --- |
| [Get Memory History](actions/get-memory-history.md) | GET | Retrieves a memory history from Mem0. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Mem0. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an organization from Mem0. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Mem0. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Mem0. |

### Organization Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Organization Member](actions/add-organization-member.md) | POST | Adds a member to an organization in Mem0. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves organization members from Mem0. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Mem0. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from Mem0. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Mem0. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Mem0. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | POST | Adds a member to a project in Mem0. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Mem0. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Mem0. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Mem0. |
| [List Project Webhooks](actions/list-project-webhooks.md) | GET | Retrieves project webhooks from Mem0. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Mem0. |

