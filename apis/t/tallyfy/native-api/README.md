# Tallyfy: Native API Reference

A consolidated summary of Tallyfy's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://tallyfy.com/products/pro/integrations/open-api/
- **OpenAPI specification:** https://api.tallyfy.com/docs/index
- **API base URL:** `https://api.tallyfy.com`

## Authentication

### Personal Access Token

Use a Tallyfy personal access token as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tallyfy.com/products/pro/integrations/open-api/code-samples/authentication/personal-access-token/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org` | path | `string` | yes | The Tallyfy organization ID used in org-scoped API paths. |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Process Task](actions/complete-process-task.md) | `POST /organizations/:org/runs/:run_id/completed-tasks` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Create Guest](actions/create-guest.md) | `POST /organizations/:org/guests` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/guests/) |
| [Create Process](actions/create-process.md) | `POST /organizations/:org/runs` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Create Task](actions/create-task.md) | `POST /organizations/:org/tasks` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/tasks/) |
| [Create Template](actions/create-template.md) | `POST /organizations/:org/checklists` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [Create Template With Steps](actions/create-template-with-steps.md) | `POST /organizations/:org/checklists-with-steps` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [Get Current Member](actions/get-current-member.md) | `GET /organizations/:org/me` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/members/) |
| [Get Process](actions/get-process.md) | `GET /organizations/:org/runs/:run_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Get Process Task](actions/get-process-task.md) | `GET /organizations/:org/runs/:run_id/tasks/:id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Get Task](actions/get-task.md) | `GET /organizations/:org/tasks/:task_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/tasks/) |
| [Get Template](actions/get-template.md) | `GET /organizations/:org/checklists/:checklist_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [List Checklists](actions/list-checklists.md) | `GET /organizations/:org/checklists-list` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [List Guests](actions/list-guests.md) | `GET /organizations/:org/guests` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/guests/) |
| [List Process Tasks](actions/list-process-tasks.md) | `GET /organizations/:org/runs/:run_id/tasks` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [List Processes](actions/list-processes.md) | `GET /organizations/:org/runs` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [List Tags](actions/list-tags.md) | `GET /organizations/:org/tags` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/tags/) |
| [List Tasks](actions/list-tasks.md) | `GET /organizations/:org/tasks` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/tasks/) |
| [List Templates](actions/list-templates.md) | `GET /organizations/:org/checklists` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [List Users](actions/list-users.md) | `GET /organizations/:org/users-list` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/members/) |
| [Reopen Process Task](actions/reopen-process-task.md) | `DELETE /organizations/:org/runs/:run_id/completed-tasks/:task_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Search Tasks](actions/search-tasks.md) | `POST /organizations/:org/checklists/search/tasks` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
| [Update Process](actions/update-process.md) | `PUT /organizations/:org/runs/:run_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Update Process Task](actions/update-process-task.md) | `PUT /organizations/:org/runs/:run_id/tasks/:id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/) |
| [Update Task](actions/update-task.md) | `PUT /organizations/:org/tasks/:task_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/tasks/) |
| [Update Template](actions/update-template.md) | `PUT /organizations/:org/checklists/:checklist_id` | [docs](https://tallyfy.com/products/pro/integrations/open-api/code-samples/templates/) |
