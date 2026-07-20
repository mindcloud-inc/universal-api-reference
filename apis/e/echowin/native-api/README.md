# echowin: Native API Reference

A consolidated summary of echowin's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://echo.win/api-docs
- **API base URL:** `https://echo.win/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://echo.win/api-docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.totalPages`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Assignments](actions/add-contact-assignments.md) | `POST /contacts/:contactId/assignments` | [docs](https://echo.win/api-docs/contacts#add-assignments) |
| [Add Contact To Boards](actions/add-contact-to-boards.md) | `POST /contacts/:contactId/boards` | [docs](https://echo.win/api-docs/contacts#assign-contact-boards) |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | `POST /contacts/bulk` | [docs](https://echo.win/api-docs/contacts#bulk-create) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://echo.win/api-docs/contacts#create-contact) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /contacts/:contactId/notes` | [docs](https://echo.win/api-docs/contacts#create-note) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://echo.win/api-docs/contacts#create-tag) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactId` | [docs](https://echo.win/api-docs/contacts#delete-contact) |
| [Get Agent Instructions](actions/get-agent-instructions.md) | `GET /agents/:agentId/instructions` | [docs](https://echo.win/api-docs/agents#get-instructions) |
| [Get Agent Knowledgebase](actions/get-agent-knowledgebase.md) | `GET /agents/:agentId/knowledgebase` | [docs](https://echo.win/api-docs/knowledgebase#agent-knowledgebase) |
| [Get Call](actions/get-call.md) | `GET /calls/:callId` | [docs](https://echo.win/api-docs/calls#get-call) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://echo.win/api-docs/contacts#get-contact) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://echo.win/api-docs/agents#list-agents) |
| [List Boards](actions/list-boards.md) | `GET /boards` | [docs](https://echo.win/api-docs/contacts#list-boards) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://echo.win/api-docs/calls#list-calls) |
| [List Contact Assignments](actions/list-contact-assignments.md) | `GET /contacts/:contactId/assignments` | [docs](https://echo.win/api-docs/contacts#list-assignments) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET /contacts/custom-fields` | [docs](https://echo.win/api-docs/contacts#custom-fields) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/:contactId/notes` | [docs](https://echo.win/api-docs/contacts#list-notes) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://echo.win/api-docs/contacts#list-contacts) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://echo.win/api-docs/contacts#list-tags) |
| [Replace Contact Assignments](actions/replace-contact-assignments.md) | `PUT /contacts/:contactId/assignments` | [docs](https://echo.win/api-docs/contacts#replace-assignments) |
| [Search Agent Knowledgebase](actions/search-agent-knowledgebase.md) | `GET /agents/:agentId/knowledgebase/search` | [docs](https://echo.win/api-docs/knowledgebase#agent-search) |
| [Update Agent Instructions](actions/update-agent-instructions.md) | `PUT /agents/:agentId/instructions` | [docs](https://echo.win/api-docs/agents#update-instructions) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contactId` | [docs](https://echo.win/api-docs/contacts#update-contact) |
| [Update Contact Boards](actions/update-contact-boards.md) | `PUT /contacts/:contactId/boards` | [docs](https://echo.win/api-docs/contacts#update-contact-boards) |
