# Fivetran: Native API Reference

A consolidated summary of Fivetran's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://fivetran.com/docs/rest-api/getting-started
- **OpenAPI specification:** https://fivetran.com/assets-docs/openapi/file_v1.json
- **API base URL:** `https://api.fivetran.com/v1`

## Authentication

### API Key

Provide your Fivetran API key and API secret. MindCloud sends them as HTTP Basic authentication using the documented api_key:api_secret format.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · The Fivetran API secret paired with the API key. Fivetran shows this value only when the secret is generated.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://fivetran.com/docs/rest-api/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `data.next_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connect Card](actions/create-connect-card.md) | `POST /connections/[:connectionId]/connect-card` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Create Connection](actions/create-connection.md) | `POST /connections` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Create Destination](actions/create-destination.md) | `POST /destinations` | [docs](https://fivetran.com/docs/rest-api/api-reference/destination) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://fivetran.com/docs/rest-api/api-reference/account) |
| [Get Connection](actions/get-connection.md) | `GET /connections/[:connectionId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Get Connection Schema Config](actions/get-connection-schema-config.md) | `GET /connections/[:connectionId]/schemas` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Get Connection State](actions/get-connection-state.md) | `GET /connections/[:connectionId]/state` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Get Connector Type Metadata](actions/get-connector-type-metadata.md) | `GET /metadata/connector-types/[:service]` | [docs](https://fivetran.com/docs/rest-api/api-reference/connector-metadata) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/[:destinationId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/destination) |
| [Get Group](actions/get-group.md) | `GET /groups/[:groupId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [Get Group Public SSH Key](actions/get-group-public-ssh-key.md) | `GET /groups/[:groupId]/public-key` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [Get Source Table Columns Config](actions/get-source-table-columns-config.md) | `GET /connections/[:connectionId]/schemas/[:schema]/tables/[:table]/columns` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Get Transformation](actions/get-transformation.md) | `GET /transformations/[:transformationId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/transformation) |
| [Get Transformation Project](actions/get-transformation-project.md) | `GET /transformation-projects/[:projectId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/transformation-project) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/[:webhookId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/webhook) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [List Connector Types](actions/list-connector-types.md) | `GET /metadata/connector-types` | [docs](https://fivetran.com/docs/rest-api/api-reference/connector-metadata) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://fivetran.com/docs/rest-api/api-reference/destination) |
| [List Group Connections](actions/list-group-connections.md) | `GET /groups/[:groupId]/connections` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/[:groupId]/users` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
| [List Transformation Projects](actions/list-transformation-projects.md) | `GET /transformation-projects` | [docs](https://fivetran.com/docs/rest-api/api-reference/transformation-project) |
| [List Transformations](actions/list-transformations.md) | `GET /transformations` | [docs](https://fivetran.com/docs/rest-api/api-reference/transformation) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://fivetran.com/docs/rest-api/api-reference/webhook) |
| [Reload Connection Schema Config](actions/reload-connection-schema-config.md) | `POST /connections/[:connectionId]/schemas/reload` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Re-sync Connection](actions/resync-connection.md) | `POST /connections/[:connectionId]/resync` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Re-sync Connection Table Data](actions/resync-connection-table-data.md) | `POST /connections/[:connectionId]/schemas/tables/resync` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Run Connection Setup Tests](actions/run-connection-setup-tests.md) | `POST /connections/[:connectionId]/test` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Run Destination Setup Tests](actions/run-destination-setup-tests.md) | `POST /destinations/[:destinationId]/test` | [docs](https://fivetran.com/docs/rest-api/api-reference/destination) |
| [Run Transformation](actions/run-transformation.md) | `POST /transformations/[:transformationId]/run` | [docs](https://fivetran.com/docs/rest-api/api-reference/transformation) |
| [Set Up Connection Schema Config](actions/set-up-connection-schema-config.md) | `POST /connections/[:connectionId]/schemas` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Sync Connection](actions/sync-connection.md) | `POST /connections/[:connectionId]/sync` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Update Connection](actions/update-connection.md) | `PATCH /connections/[:connectionId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Update Connection Column Config](actions/update-connection-column-config.md) | `PATCH /connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]/columns/[:columnName]` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Update Connection Schema Config](actions/update-connection-schema-config.md) | `PATCH /connections/[:connectionId]/schemas` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Update Connection State](actions/update-connection-state.md) | `PATCH /connections/[:connectionId]/state` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection) |
| [Update Connection Table Config](actions/update-connection-table-config.md) | `PATCH /connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]` | [docs](https://fivetran.com/docs/rest-api/api-reference/connection-schema) |
| [Update Destination](actions/update-destination.md) | `PATCH /destinations/[:destinationId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/destination) |
| [Update Group](actions/update-group.md) | `PATCH /groups/[:groupId]` | [docs](https://fivetran.com/docs/rest-api/api-reference/group) |
