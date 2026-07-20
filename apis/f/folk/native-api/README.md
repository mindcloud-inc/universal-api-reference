# folk: Native API Reference

A consolidated summary of folk's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://developer.folk.app/api-reference/overview
- **API base URL:** `https://api.folk.app`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.folk.app/docs/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /v1/companies` | [docs](https://developer.folk.app/api-reference/companies/create-a-company) |
| [Create Deal](actions/create-deal.md) | `POST /v1/groups/:groupId/:objectType` | [docs](https://developer.folk.app/api-reference/deals/create-a-deal) |
| [Create Interaction](actions/create-interaction.md) | `POST /v1/interactions` | [docs](https://developer.folk.app/api-reference/interactions/create-an-interaction) |
| [Create Note](actions/create-note.md) | `POST /v1/notes` | [docs](https://developer.folk.app/api-reference/notes/create-a-note) |
| [Create Person](actions/create-person.md) | `POST /v1/people` | [docs](https://developer.folk.app/api-reference/people/create-a-person) |
| [Create Reminder](actions/create-reminder.md) | `POST /v1/reminders` | [docs](https://developer.folk.app/api-reference/reminders/create-a-reminder) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://developer.folk.app/api-reference/webhooks/create-a-webhook) |
| [Delete Company](actions/delete-company.md) | `DELETE /v1/companies/:companyId` | [docs](https://developer.folk.app/api-reference/companies/delete-a-company) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /v1/groups/:groupId/:objectType/:objectId` | [docs](https://developer.folk.app/api-reference/deals/delete-a-deal) |
| [Delete Note](actions/delete-note.md) | `DELETE /v1/notes/:noteId` | [docs](https://developer.folk.app/api-reference/notes/delete-a-note) |
| [Delete Person](actions/delete-person.md) | `DELETE /v1/people/:personId` | [docs](https://developer.folk.app/api-reference/people/delete-a-person) |
| [Delete Reminder](actions/delete-reminder.md) | `DELETE /v1/reminders/:reminderId` | [docs](https://developer.folk.app/api-reference/reminders/delete-a-reminder) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:webhookId` | [docs](https://developer.folk.app/api-reference/webhooks/delete-a-webhook) |
| [Get Company](actions/get-company.md) | `GET /v1/companies/:companyId` | [docs](https://developer.folk.app/api-reference/companies/get-a-company) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/users/me` | [docs](https://developer.folk.app/api-reference/users/get-the-current-user) |
| [Get Deal](actions/get-deal.md) | `GET /v1/groups/:groupId/:objectType/:objectId` | [docs](https://developer.folk.app/api-reference/deals/get-a-deal) |
| [Get Note](actions/get-note.md) | `GET /v1/notes/:noteId` | [docs](https://developer.folk.app/api-reference/notes/get-a-note) |
| [Get Person](actions/get-person.md) | `GET /v1/people/:personId` | [docs](https://developer.folk.app/api-reference/people/get-a-person) |
| [Get Reminder](actions/get-reminder.md) | `GET /v1/reminders/:reminderId` | [docs](https://developer.folk.app/api-reference/reminders/get-a-reminder) |
| [Get User](actions/get-user.md) | `GET /v1/users/:userId` | [docs](https://developer.folk.app/api-reference/users/get-a-user) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:webhookId` | [docs](https://developer.folk.app/api-reference/webhooks/get-a-webhook) |
| [List Companies](actions/list-companies.md) | `GET /v1/companies` | [docs](https://developer.folk.app/api-reference/companies/list-companies) |
| [List Deals](actions/list-deals.md) | `GET /v1/groups/:groupId/:objectType` | [docs](https://developer.folk.app/api-reference/deals/list-deals) |
| [List Group Custom Fields](actions/list-group-custom-fields.md) | `GET /v1/groups/:groupId/custom-fields/:entityType` | [docs](https://developer.folk.app/api-reference/groups/list-group-custom-fields) |
| [List Groups](actions/list-groups.md) | `GET /v1/groups` | [docs](https://developer.folk.app/api-reference/groups/list-groups) |
| [List Notes](actions/list-notes.md) | `GET /v1/notes` | [docs](https://developer.folk.app/api-reference/notes/list-notes) |
| [List People](actions/list-people.md) | `GET /v1/people` | [docs](https://developer.folk.app/api-reference/people/list-people) |
| [List Reminders](actions/list-reminders.md) | `GET /v1/reminders` | [docs](https://developer.folk.app/api-reference/reminders/list-reminders) |
| [List Users](actions/list-users.md) | `GET /v1/users` | [docs](https://developer.folk.app/api-reference/users/list-users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://developer.folk.app/api-reference/webhooks/list-webhooks) |
| [Update Company](actions/update-company.md) | `PATCH /v1/companies/:companyId` | [docs](https://developer.folk.app/api-reference/companies/update-a-company) |
| [Update Deal](actions/update-deal.md) | `PATCH /v1/groups/:groupId/:objectType/:objectId` | [docs](https://developer.folk.app/api-reference/deals/update-a-deal) |
| [Update Note](actions/update-note.md) | `PATCH /v1/notes/:noteId` | [docs](https://developer.folk.app/api-reference/notes/update-a-note) |
| [Update Person](actions/update-person.md) | `PATCH /v1/people/:personId` | [docs](https://developer.folk.app/api-reference/people/update-a-person) |
| [Update Reminder](actions/update-reminder.md) | `PATCH /v1/reminders/:reminderId` | [docs](https://developer.folk.app/api-reference/reminders/update-a-reminder) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /v1/webhooks/:webhookId` | [docs](https://developer.folk.app/api-reference/webhooks/update-a-webhook) |
