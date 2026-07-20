# Mem0: Native API Reference

A consolidated summary of Mem0's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.mem0.ai/api-reference
- **API base URL:** `https://api.mem0.ai`

## Authentication

### API Key

Mem0 API key authentication. Requests use the shared Authorization header with the Token prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mem0.ai/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Memories](actions/add-memories.md) | `POST /v1/memories/` | [docs](https://docs.mem0.ai/api-reference/memory/add-memories) |
| [Add Organization Member](actions/add-organization-member.md) | `POST /api/v1/orgs/organizations/:org_id/members/` | [docs](https://docs.mem0.ai/api-reference/organization/add-org-member) |
| [Add Project Member](actions/add-project-member.md) | `POST /api/v1/orgs/organizations/:org_id/projects/:project_id/members/` | [docs](https://docs.mem0.ai/api-reference/project/add-project-member) |
| [Batch Delete Memories](actions/batch-delete-memories.md) | `DELETE /v1/batch/` | [docs](https://docs.mem0.ai/api-reference/memory/batch-delete) |
| [Batch Update Memories](actions/batch-update-memories.md) | `PUT /v1/batch/` | [docs](https://docs.mem0.ai/api-reference/memory/batch-update) |
| [Create Memory Export](actions/create-memory-export.md) | `POST /v1/exports/` | [docs](https://docs.mem0.ai/api-reference/memory/create-memory-export) |
| [Create Organization](actions/create-organization.md) | `POST /api/v1/orgs/organizations/` | [docs](https://docs.mem0.ai/api-reference/organization/create-org) |
| [Create Project](actions/create-project.md) | `POST /api/v1/orgs/organizations/:org_id/projects/` | [docs](https://docs.mem0.ai/api-reference/project/create-project) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v1/webhooks/projects/:project_id/` | [docs](https://docs.mem0.ai/api-reference/webhook/create-webhook) |
| [Delete Entity](actions/delete-entity.md) | `DELETE /v2/entities/:entity_type/:entity_id/` | [docs](https://docs.mem0.ai/api-reference/entities/delete-user) |
| [Delete Memories](actions/delete-memories.md) | `DELETE /v1/memories/` | [docs](https://docs.mem0.ai/api-reference/memory/delete-memories) |
| [Delete Memory](actions/delete-memory.md) | `DELETE /v1/memories/:memory_id/` | [docs](https://docs.mem0.ai/api-reference/memory/delete-memory) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /api/v1/orgs/organizations/:org_id/` | [docs](https://docs.mem0.ai/api-reference/organization/delete-org) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/orgs/organizations/:org_id/projects/:project_id/` | [docs](https://docs.mem0.ai/api-reference/project/delete-project) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v1/webhooks/:webhook_id/` | [docs](https://docs.mem0.ai/api-reference/webhook/delete-webhook) |
| [Get Event](actions/get-event.md) | `GET /v1/event/:event_id/` | [docs](https://docs.mem0.ai/api-reference/events/get-event) |
| [Get Memory](actions/get-memory.md) | `GET /v1/memories/:memory_id/` | [docs](https://docs.mem0.ai/api-reference/memory/get-memory) |
| [Get Memory Export](actions/get-memory-export.md) | `POST /v1/exports/get` | [docs](https://docs.mem0.ai/api-reference/memory/get-memory-export) |
| [Get Memory History](actions/get-memory-history.md) | `GET /v1/memories/:memory_id/history/` | [docs](https://docs.mem0.ai/api-reference/memory/history-memory) |
| [Get Organization](actions/get-organization.md) | `GET /api/v1/orgs/organizations/:org_id/` | [docs](https://docs.mem0.ai/api-reference/organization/get-org) |
| [Get Project](actions/get-project.md) | `GET /api/v1/orgs/organizations/:org_id/projects/:project_id/` | [docs](https://docs.mem0.ai/api-reference/project/get-project) |
| [List Entities](actions/list-entities.md) | `GET /v1/entities/` | [docs](https://docs.mem0.ai/api-reference/entities/get-users) |
| [List Events](actions/list-events.md) | `GET /v1/events/` | [docs](https://docs.mem0.ai/api-reference/events/get-events) |
| [List Memories](actions/list-memories.md) | `POST /v2/memories/` | [docs](https://docs.mem0.ai/api-reference/memory/get-memories) |
| [List Organization Members](actions/list-organization-members.md) | `GET /api/v1/orgs/organizations/:org_id/members/` | [docs](https://docs.mem0.ai/api-reference/organization/get-org-members) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v1/orgs/organizations/` | [docs](https://docs.mem0.ai/api-reference/organization/get-orgs) |
| [List Project Members](actions/list-project-members.md) | `GET /api/v1/orgs/organizations/:org_id/projects/:project_id/members/` | [docs](https://docs.mem0.ai/api-reference/project/get-project-members) |
| [List Project Webhooks](actions/list-project-webhooks.md) | `GET /api/v1/webhooks/projects/:project_id/` | [docs](https://docs.mem0.ai/api-reference/webhook/get-webhook) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/orgs/organizations/:org_id/projects/` | [docs](https://docs.mem0.ai/api-reference/project/get-projects) |
| [Search Memories](actions/search-memories.md) | `POST /v2/memories/search/` | [docs](https://docs.mem0.ai/api-reference/memory/search-memories) |
| [Submit Memory Feedback](actions/submit-memory-feedback.md) | `POST /v1/feedback/` | [docs](https://docs.mem0.ai/api-reference/memory/feedback) |
| [Update Memory](actions/update-memory.md) | `PUT /v1/memories/:memory_id/` | [docs](https://docs.mem0.ai/api-reference/memory/update-memory) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/v1/webhooks/:webhook_id/` | [docs](https://docs.mem0.ai/api-reference/webhook/update-webhook) |
