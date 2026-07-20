# Spondyr: Native API Reference

A consolidated summary of Spondyr's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://client.spondyr.io/Public/Public/APIDocumentation
- **API base URL:** `https://client.spondyr.io/api/v1.0.0/`

## Authentication

### Spondyr API Credentials

Use the Spondyr subscription API key and application token from your Spondyr account.

### Credentials

- **API Key:** `apiKey` · required · Your Spondyr subscription API key.
- **Application Token:** `applicationToken` · required · Your Spondyr application token.

[Official authentication documentation](https://client.spondyr.io/Public/Public/Documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Condition](actions/create-condition.md) | `POST /Condition` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Create Event Type](actions/create-event-type.md) | `POST /EventType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Create Transaction Type](actions/create-transaction-type.md) | `POST /TransactionType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Delete Condition](actions/delete-condition.md) | `DELETE /Condition` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Delete Event Type](actions/delete-event-type.md) | `DELETE /EventType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Delete Transaction Type](actions/delete-transaction-type.md) | `DELETE /TransactionType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Get Condition](actions/get-condition.md) | `GET /Condition` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Get Event Type](actions/get-event-type.md) | `GET /EventType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Get Transaction Type](actions/get-transaction-type.md) | `GET /TransactionType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [List Conditions](actions/list-conditions.md) | `GET /Conditions` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [List Event Types](actions/list-event-types.md) | `GET /EventTypes` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [List Transaction Types](actions/list-transaction-types.md) | `GET /TransactionTypes` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Update Condition](actions/update-condition.md) | `PUT /Condition` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Update Event Type](actions/update-event-type.md) | `PUT /EventType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
| [Update Transaction Type](actions/update-transaction-type.md) | `PUT /TransactionType` | [docs](https://client.spondyr.io/Public/Public/APIDocumentation) |
