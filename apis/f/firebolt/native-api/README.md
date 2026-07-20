# Firebolt: Native API Reference

A consolidated summary of Firebolt's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api
- **OpenAPI specification:** https://raw.githubusercontent.com/firebolt-db/openapi/main/specification/yaml/firebolt_query_v2.3.yaml
- **API base URL:** `https://api.app.firebolt.io`

## Authentication

### OAuth 2.0

Authenticate Firebolt with a service account client ID and secret.

### Credentials

- **Account name:** `accountName` · required · The Firebolt account name used to retrieve the system engine URL.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://id.app.firebolt.io/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.firebolt.io/guides/managing-your-organization/service-accounts)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Query](actions/cancel-query.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/queries/cancel) |
| [Check Async Query Status](actions/check-async-query-status.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-api/using-async-queries) |
| [Copy From S3](actions/copy-from-s3.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/copy-from) |
| [Copy To S3](actions/copy-to-s3.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/copy-to) |
| [Create Database](actions/create-database.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/data-definition/create-database) |
| [Create Engine](actions/create-engine.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/engines/create-engine) |
| [Create Role](actions/create-role.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/access-control/create-role) |
| [Create User](actions/create-user.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/access-control/create-user) |
| [Create View](actions/create-view.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/data-definition/create-view) |
| [Delete Engine](actions/delete-engine.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/engines/drop-engine) |
| [Delete Rows](actions/delete-rows.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/delete) |
| [Delete View](actions/delete-view.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-definition/drop-view) |
| [Describe Object](actions/describe-object.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/describe) |
| [Explain Query](actions/explain-query.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/queries/explain) |
| [Firebolt Query Helper](actions/firebolt-query-helper.md) | `POST https://:engineHost?engine=:engineName&database=:database&output_format=JSON_Compact` | [docs](https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api) |
| [Get Engine Metrics History](actions/get-engine-metrics-history.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/information-schema/engine-metrics-history) |
| [Get Engine Query History](actions/get-engine-query-history.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/information-schema/engine-query-history) |
| [Get Storage History](actions/get-storage-history.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/information-schema/storage-history) |
| [Get System Engine URL](actions/get-system-engine-url.md) | `GET /web/v3/account/:accountName/engineUrl` | [docs](https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api) |
| [Grant Privileges](actions/grant-privileges.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/access-control/grant) |
| [Insert Rows](actions/insert-rows.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/insert) |
| [List Columns](actions/list-columns.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-columns) |
| [List Databases](actions/list-databases.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-catalogs) |
| [List Engines](actions/list-engines.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-engines) |
| [List Indexes](actions/list-indexes.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-indexes) |
| [List Running Queries](actions/list-running-queries.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/information-schema/engine-running-queries) |
| [List Tables](actions/list-tables.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-tables) |
| [List Views](actions/list-views.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/metadata/show-views) |
| [Merge Rows](actions/merge-rows.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/merge) |
| [Recommend DDL](actions/recommend-ddl.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-sql/commands/queries/recommend_ddl) |
| [Run Async SQL Query](actions/run-async-sql-query.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-api/using-async-queries) |
| [Run Sync SQL Query](actions/run-sync-sql-query.md) | `POST https://:engineUrl` | [docs](https://docs.firebolt.io/reference-api/using-sync-queries) |
| [Start Engine](actions/start-engine.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/engines/start-engine) |
| [Stop Engine](actions/stop-engine.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/engines/stop-engine) |
| [Update Database](actions/update-database.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-definition/alter-database) |
| [Update Engine](actions/update-engine.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/engines/alter-engine) |
| [Update Location](actions/update-location.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-definition/alter-location) |
| [Update Rows](actions/update-rows.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/update) |
| [Vacuum Table](actions/vacuum-table.md) | `POST https://:engineHost` | [docs](https://docs.firebolt.io/reference-sql/commands/data-management/vacuum) |
