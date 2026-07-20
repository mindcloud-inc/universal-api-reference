# Doppler Marketing Automation: Native API Reference

A consolidated summary of Doppler Marketing Automation's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://restapi.fromdoppler.com/docs/
- **API base URL:** `https://restapi.fromdoppler.com`

## Authentication

### API Key

Use a Doppler REST API key. Doppler recommends sending it in the Authorization header as `token <API key>`.

### Credentials

- **API Key:** `apiKey` · required
- **Account Name:** `accountName` · required · Doppler account email address used in REST API paths such as /accounts/{accountName}.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://restapi.fromdoppler.com/docs/gettingstarted)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountName` | path | `string` | yes | Doppler account email address used in REST API paths such as /accounts/{accountName}. |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Associate Subscriber](actions/associate-subscriber.md) | `POST /accounts/:accountName/lists/:listId/subscribers` | [docs](https://restapi.fromdoppler.com/docs/rels/associate-subscriber) |
| [Create List](actions/create-list.md) | `POST /accounts/:accountName/lists` | [docs](https://restapi.fromdoppler.com/docs/rels/create-list) |
| [Delete List](actions/delete-list.md) | `DELETE /accounts/:accountName/lists/:listId` | [docs](https://restapi.fromdoppler.com/docs/rels/delete-list) |
| [Get Account Home](actions/get-account-home.md) | `GET /accounts/:accountName` | [docs](https://restapi.fromdoppler.com/docs/rels/get-account-home) |
| [Get API Index](actions/get-api-index.md) | `GET /` | [docs](https://restapi.fromdoppler.com/docs/rels/get-index) |
| [Get List](actions/get-list.md) | `GET /accounts/:accountName/lists/:listId` | [docs](https://restapi.fromdoppler.com/docs/rels/get-list) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /accounts/:accountName/subscribers/:email` | [docs](https://restapi.fromdoppler.com/docs/rels/get-subscriber) |
| [Get Task](actions/get-task.md) | `GET /accounts/:accountName/tasks/:taskId` | [docs](https://restapi.fromdoppler.com/docs/rels/get-task) |
| [Import Subscribers](actions/import-subscribers.md) | `POST /accounts/:accountName/subscribers/import` | [docs](https://restapi.fromdoppler.com/docs/rels/import-subscribers) |
| [Import Subscribers To List](actions/import-subscribers-to-list.md) | `POST /accounts/:accountName/lists/:listId/subscribers/import` | [docs](https://restapi.fromdoppler.com/docs/rels/import-subscribers) |
| [Import Unsubscribed Subscribers](actions/import-unsubscribed-subscribers.md) | `POST /accounts/:accountName/unsubscribed/import` | [docs](https://restapi.fromdoppler.com/docs/rels/import-unsubscribed) |
| [List Fields](actions/list-fields.md) | `GET /accounts/:accountName/fields` | [docs](https://restapi.fromdoppler.com/docs/rels/get-field-collection) |
| [List Lists](actions/list-lists.md) | `GET /accounts/:accountName/lists` | [docs](https://restapi.fromdoppler.com/docs/rels/get-list-collection) |
| [List Subscribers](actions/list-subscribers.md) | `GET /accounts/:accountName/lists/:listId/subscribers` | [docs](https://restapi.fromdoppler.com/docs/rels/get-subscriber-collection) |
| [List Tasks](actions/list-tasks.md) | `GET /accounts/:accountName/tasks` | [docs](https://restapi.fromdoppler.com/docs/rels/get-task-collection) |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | `GET /accounts/:accountName/unsubscribed` | [docs](https://restapi.fromdoppler.com/docs/rels/get-unsubscribed-collection) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /accounts/:accountName/unsubscribed` | [docs](https://restapi.fromdoppler.com/docs/rels/unsubscribe) |
| [Update List](actions/update-list.md) | `PUT /accounts/:accountName/lists/:listId` | [docs](https://restapi.fromdoppler.com/docs/rels/edit-list) |
