# OkoCRM: Native API Reference

A consolidated summary of OkoCRM's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://okocrm.com/api/
- **API base URL:** `https://api.okocrm.com/v2`

## Authentication

### API key

Use an OkoCRM API token. MindCloud sends it as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://okocrm.com/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete task with comment](actions/complete-task-with-comment.md) | `POST /tasks/done/[:id]` | [docs](https://okocrm.com/api/) |
| [Create company](actions/create-company.md) | `POST /companies/` | [docs](https://okocrm.com/api/) |
| [Create contact](actions/create-contact.md) | `POST /contacts/` | [docs](https://okocrm.com/api/) |
| [Create deal](actions/create-deal.md) | `POST /leads/` | [docs](https://okocrm.com/api/) |
| [Create note](actions/create-note.md) | `POST /notes/note` | [docs](https://okocrm.com/api/) |
| [Create task](actions/create-task.md) | `POST /tasks/` | [docs](https://okocrm.com/api/) |
| [Delete company](actions/delete-company.md) | `DELETE /companies/[:company_id]/` | [docs](https://okocrm.com/api/) |
| [Delete contact](actions/delete-contact.md) | `DELETE /contacts/[:contact_id]/` | [docs](https://okocrm.com/api/) |
| [Delete deal](actions/delete-deal.md) | `DELETE /leads/[:lead_id]/` | [docs](https://okocrm.com/api/) |
| [Delete task](actions/delete-task.md) | `DELETE /tasks/[:task_id]/` | [docs](https://okocrm.com/api/) |
| [Get company](actions/get-company.md) | `GET /companies/[:company_id]/` | [docs](https://okocrm.com/api/) |
| [Get contact](actions/get-contact.md) | `GET /contacts/[:contact_id]/` | [docs](https://okocrm.com/api/) |
| [Get deal](actions/get-deal.md) | `GET /leads/[:lead_id]/` | [docs](https://okocrm.com/api/) |
| [Link company entities](actions/link-company-entities.md) | `POST /companies/[:company_id]/link/` | [docs](https://okocrm.com/api/) |
| [Link contact entities](actions/link-contact-entities.md) | `POST /contacts/[:contact_id]/link/` | [docs](https://okocrm.com/api/) |
| [Link deal entities](actions/link-deal-entities.md) | `POST /leads/[:lead_id]/link/` | [docs](https://okocrm.com/api/) |
| [List cities](actions/list-cities.md) | `GET /cities/` | [docs](https://okocrm.com/api/) |
| [List companies](actions/list-companies.md) | `GET /companies/` | [docs](https://okocrm.com/api/) |
| [List contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://okocrm.com/api/) |
| [List deals](actions/list-deals.md) | `GET /leads/` | [docs](https://okocrm.com/api/) |
| [List fields](actions/list-fields.md) | `GET /fields/` | [docs](https://okocrm.com/api/) |
| [List notes](actions/list-notes.md) | `GET /notes/` | [docs](https://okocrm.com/api/) |
| [List pipeline stages](actions/list-pipeline-stages.md) | `GET /pipelines/stages/[:pipeline_id]` | [docs](https://okocrm.com/api/) |
| [List pipelines](actions/list-pipelines.md) | `GET /pipelines/` | [docs](https://okocrm.com/api/) |
| [List task types](actions/list-task-types.md) | `GET /tasks/types/` | [docs](https://okocrm.com/api/) |
| [List tasks](actions/list-tasks.md) | `GET /tasks/` | [docs](https://okocrm.com/api/) |
| [List users](actions/list-users.md) | `GET /users/` | [docs](https://okocrm.com/api/) |
| [Update company](actions/update-company.md) | `PUT /companies/[:company_id]/` | [docs](https://okocrm.com/api/) |
| [Update contact](actions/update-contact.md) | `PUT /contacts/[:contact_id]/` | [docs](https://okocrm.com/api/) |
| [Update deal](actions/update-deal.md) | `PUT /leads/[:lead_id]/` | [docs](https://okocrm.com/api/) |
| [Update task](actions/update-task.md) | `PUT /tasks/[:task_id]/` | [docs](https://okocrm.com/api/) |
