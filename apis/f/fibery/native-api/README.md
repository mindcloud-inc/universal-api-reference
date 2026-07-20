# Fibery: Native API Reference

A consolidated summary of Fibery's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://the.fibery.io/@public/User_Guide/Guide/Fibery-API-Overview-279
- **API base URL:** `https://{account}.fibery.io/api`

## Authentication

### API Token

Connect Fibery using your workspace account and API token.

### Credentials

- **API Key:** `apiKey` · required
- **Account:** `account` · required · Workspace subdomain used in YOUR_ACCOUNT.fibery.io.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://the.fibery.io/@public/User_Guide/Guide/REST-API-259)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Collection Items](actions/add-collection-items.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Attach File To Entity](actions/attach-file-to-entity.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265) |
| [Create Entity](actions/create-entity.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Create Field](actions/create-field.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Field-API-263) |
| [Create Or Update Entities](actions/create-or-update-entities.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Create Type](actions/create-type.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/v2` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Webhooks-258) |
| [Delete Entity](actions/delete-entity.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Delete Field](actions/delete-field.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Field-API-263) |
| [Delete Type](actions/delete-type.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/v2/:webhookId` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Webhooks-258) |
| [Download File](actions/download-file.md) | `GET /files/:secret` | [docs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265) |
| [Get Schema](actions/get-schema.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Schema-API-261) |
| [Get Temporary Public File URLs](actions/get-temporary-public-file-urls.md) | `POST /files/sign-urls` | [docs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265) |
| [GraphQL Mutation](actions/graphql-mutation.md) | `POST /graphql/space/:space` | [docs](https://the.fibery.io/@public/User_Guide/Guide/GraphQL-mutations-256) |
| [GraphQL Query](actions/graphql-query.md) | `POST /graphql/space/:space` | [docs](https://the.fibery.io/@public/User_Guide/Guide/GraphQL-queries-255) |
| [List GraphQL Endpoints](actions/list-graphql-endpoints.md) | `GET /graphql` | [docs](https://the.fibery.io/@public/User_Guide/Guide/GraphQL-API-254) |
| [Query Entities](actions/query-entities.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Remove Collection Items](actions/remove-collection-items.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Rename Type](actions/rename-type.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262) |
| [Update Entity](actions/update-entity.md) | `POST /commands` | [docs](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265) |
| [Upload File From URL](actions/upload-file-from-url.md) | `POST /files/from-url` | [docs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265) |
