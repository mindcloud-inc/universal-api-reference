# Endear: Native API Reference

A consolidated summary of Endear's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.endearhq.com/docs/introduction
- **API base URL:** `https://api.endearhq.com`

## Authentication

### API Key

Use an Endear GraphQL Admin API key sent in the X-Endear-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.endearhq.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `first` in the request body to set the page size (default 25; accepted range 1–100). Use `after` in the request body as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Users To Customer](actions/assign-users-to-customer.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Assign Users To Task](actions/assign-users-to-task.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Bulk Upsert External Customers](actions/bulk-upsert-external-customers.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/bulkupsert-endpoint-guidance) |
| [Bulk Upsert External Products](actions/bulk-upsert-external-products.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/bulkupsert-endpoint-guidance) |
| [Create Customer](actions/create-customer.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Create Customer Field](actions/create-customer-field.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Create Note](actions/create-note.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Create Note Comment](actions/create-note-comment.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Create Task](actions/create-task.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Current Brand](actions/current-brand.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Current Integration](actions/current-integration.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/authentication) |
| [Get Conversation](actions/get-conversation.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Customer Fields By IDs](actions/get-customer-fields-by-ids.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Customer Fields By Keys](actions/get-customer-fields-by-keys.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Customers By External IDs](actions/get-customers-by-external-ids.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Drafts By IDs](actions/get-drafts-by-ids.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Integration](actions/get-integration.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Message](actions/get-message.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Note](actions/get-note.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Task](actions/get-task.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get Team](actions/get-team.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Get User](actions/get-user.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [List Customer Fields](actions/list-customer-fields.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [List Integrations](actions/list-integrations.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [List Messages](actions/list-messages.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [List Teams](actions/list-teams.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [List Users](actions/list-users.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Search Conversations](actions/search-conversations.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Search Customers](actions/search-customers.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/graphql-pagination) |
| [Search Drafts](actions/search-drafts.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Search Messages](actions/search-messages.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Search Notes](actions/search-notes.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Search Tasks](actions/search-tasks.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Unassign Users From Customer](actions/unassign-users-from-customer.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Unassign Users From Task](actions/unassign-users-from-task.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Update Customer](actions/update-customer.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Update Customer Field Attributes](actions/update-customer-field-attributes.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Update Note](actions/update-note.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Update Note Comment](actions/update-note-comment.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
| [Update Task](actions/update-task.md) | `POST /graphql` | [docs](https://docs.endearhq.com/docs/introduction) |
