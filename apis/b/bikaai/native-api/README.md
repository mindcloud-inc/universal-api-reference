# Bika.ai: Native API Reference

A consolidated summary of Bika.ai's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://bika.ai/help/guide/developer/openapi
- **OpenAPI specification:** https://bika.ai/help/openapi/bika
- **API base URL:** `https://bika.ai/api/openapi/bika/v1`

## Authentication

### API Token

Authenticate with a Bika.ai API token sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bika.ai/help/guide/developer/openapi)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database Record](actions/create-database-record.md) | `POST /spaces/:spaceId/resources/databases/:nodeId/records` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Delete Database Record](actions/delete-database-record.md) | `DELETE /spaces/:spaceId/resources/databases/:nodeId/records/:recordId` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://bika.ai/help/openapi/bika) |
| [Get System Meta](actions/get-system-meta.md) | `GET /system/meta` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Get User Profile](actions/get-user-profile.md) | `GET /user/profile` | [docs](https://bika.ai/help/openapi/bika) |
| [List Automation Triggers](actions/list-automation-triggers.md) | `GET /automations/:nodeId/triggers` | [docs](https://bika.ai/help/openapi/bika) |
| [List Database Records](actions/list-database-records.md) | `GET /spaces/:spaceId/resources/databases/:nodeId/records` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [List Embed Links](actions/list-embed-links.md) | `GET /spaces/:spaceId/embed-links` | [docs](https://bika.ai/help/openapi/bika) |
| [List Outbound Webhooks](actions/list-outbound-webhooks.md) | `GET /spaces/:spaceId/outgoing-webhooks` | [docs](https://bika.ai/help/openapi/bika) |
| [List Space Nodes](actions/list-space-nodes.md) | `GET /spaces/:spaceId/nodes` | [docs](https://bika.ai/help/openapi/bika) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Register Outbound Webhook](actions/register-outbound-webhook.md) | `POST /spaces/:spaceId/outgoing-webhooks` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Update Database Record](actions/update-database-record.md) | `PATCH /spaces/:spaceId/resources/databases/:nodeId/records` | [docs](https://bika.ai/help/guide/developer/openapi) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /spaces/:spaceId/attachments` | [docs](https://bika.ai/help/guide/developer/openapi) |
