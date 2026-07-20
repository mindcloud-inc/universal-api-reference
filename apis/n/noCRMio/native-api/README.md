# noCRM.io: Native API Reference

A consolidated summary of noCRM.io's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.nocrm.io/api
- **API base URL:** `{baseUrl}/api/v2`

## Authentication

### API Key

Use a noCRM API key together with your account URL.

### Credentials

- **API Key:** `apiKey` · required
- **Account URL:** `baseUrl` · required · Your full noCRM account URL, for example https://company.nocrm.io

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nocrm.io/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead To Client Folder](actions/add-lead-to-client-folder.md) | `POST /leads/:id/add_to_client` | [docs](https://www.nocrm.io/api#add-a-lead-to-a-client-folder) |
| [Assign Lead](actions/assign-lead.md) | `POST /leads/:id/assign` | [docs](https://www.nocrm.io/api#assign-a-lead) |
| [Create Client Folder](actions/create-client-folder.md) | `POST /clients` | [docs](https://www.nocrm.io/api#create-a-client-folder) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://www.nocrm.io/api#create-a-lead) |
| [Create Lead Comment](actions/create-lead-comment.md) | `POST /leads/:lead_id/comments` | [docs](https://www.nocrm.io/api#create-a-comment-on-a-lead) |
| [Delete Client Folder](actions/delete-client-folder.md) | `DELETE /clients/:id` | [docs](https://www.nocrm.io/api#delete-a-client-folder) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/:id` | [docs](https://www.nocrm.io/api#delete-a-lead) |
| [Delete Lead Comment](actions/delete-lead-comment.md) | `DELETE /leads/:lead_id/comments/:id` | [docs](https://www.nocrm.io/api#delete-a-comment-on-a-lead) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://www.nocrm.io/api#list-the-activities) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://www.nocrm.io/api#list-the-categories) |
| [List Client Folders](actions/list-client-folders.md) | `GET /clients` | [docs](https://www.nocrm.io/api#list-the-client-folders) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://www.nocrm.io/api#list-the-fields) |
| [List Lead Action Histories](actions/list-lead-action-histories.md) | `GET /leads/:lead_id/action_histories` | [docs](https://www.nocrm.io/api#list-the-action-histories-on-a-lead) |
| [List Lead Comments](actions/list-lead-comments.md) | `GET /leads/:lead_id/comments` | [docs](https://www.nocrm.io/api#retrieve-all-comments-from-a-lead) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://www.nocrm.io/api#list-the-leads) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://www.nocrm.io/api#list-the-pipelines) |
| [List Predefined Tags](actions/list-predefined-tags.md) | `GET /predefined_tags` | [docs](https://www.nocrm.io/api#list-the-predefined-tags) |
| [List Steps](actions/list-steps.md) | `GET /steps` | [docs](https://www.nocrm.io/api#list-the-steps) |
| [List Unassigned Leads](actions/list-unassigned-leads.md) | `GET /leads/unassigned` | [docs](https://www.nocrm.io/api#list-the-unassigned-leads) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.nocrm.io/api#list-all-the-users) |
| [Retrieve Client Folder](actions/retrieve-client-folder.md) | `GET /clients/:id` | [docs](https://www.nocrm.io/api#retrieve-a-client-folder) |
| [Retrieve Lead](actions/retrieve-lead.md) | `GET /leads/:id` | [docs](https://www.nocrm.io/api#retrieve-a-lead) |
| [Retrieve Step](actions/retrieve-step.md) | `GET /steps/:id` | [docs](https://www.nocrm.io/api#retrieve-a-step) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:id` | [docs](https://www.nocrm.io/api#retrieve-a-user) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/:id` | [docs](https://www.nocrm.io/api#update-a-lead) |
| [Update Lead Comment](actions/update-lead-comment.md) | `PUT /leads/:lead_id/comments/:id` | [docs](https://www.nocrm.io/api#update-a-comment-on-a-lead) |
