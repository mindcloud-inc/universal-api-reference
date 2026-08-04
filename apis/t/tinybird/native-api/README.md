# Tinybird: Native API Reference

A consolidated summary of Tinybird's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://www.tinybird.co/docs/api-reference
- **API base URL:** `{apiHost}`

## Authentication

### Tinybird Token

Connect with a Tinybird static token.

### Credentials

- **Tinybird Token:** `apiKey` · required
- **API Host:** `apiHost` · required · Your Tinybird workspace API URL. Choose the URL for your workspace's region.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.tinybird.co/docs/forward/core-concepts/static-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Pipe Node](actions/add-pipe-node.md) | `POST v0/pipes/:name/nodes` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Alter Data Source](actions/alter-data-source.md) | `POST v0/datasources/:name/alter` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Analyze Data File](actions/analyze-data-file.md) | `POST v0/analyze` | [docs](https://www.tinybird.co/docs/api-reference/analyze-api) |
| [Append Data](actions/append-data.md) | `POST v0/datasources` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Cancel Job](actions/cancel-job.md) | `POST v0/jobs/:id/cancel` | [docs](https://www.tinybird.co/docs/api-reference/jobs-api) |
| [Create Data Source](actions/create-data-source.md) | `POST v0/datasources` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Create Environment Variable](actions/create-environment-variable.md) | `POST v0/variables` | [docs](https://www.tinybird.co/docs/api-reference/environment-variables-api) |
| [Create Pipe](actions/create-pipe.md) | `POST v0/pipes` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Create Static Token](actions/create-static-token.md) | `POST v0/tokens` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
| [Delete Data Source](actions/delete-data-source.md) | `DELETE v0/datasources/:name` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Delete Environment Variable](actions/delete-environment-variable.md) | `DELETE v0/variables/:name` | [docs](https://www.tinybird.co/docs/api-reference/environment-variables-api) |
| [Delete Matching Data](actions/delete-matching-data.md) | `POST v0/datasources/:name/delete` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Delete Pipe](actions/delete-pipe.md) | `DELETE v0/pipes/:name` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Delete Pipe Node](actions/delete-pipe-node.md) | `DELETE v0/pipes/:name/nodes/:node` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Delete Static Token](actions/delete-static-token.md) | `DELETE v0/tokens/:token` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
| [Execute SQL Query](actions/execute-sql-query.md) | `POST v0/sql` | [docs](https://www.tinybird.co/docs/api-reference/sql-api) |
| [Execute SQL Query (GET)](actions/execute-sql-query-get.md) | `GET v0/sql` | [docs](https://www.tinybird.co/docs/api-reference/query-api) |
| [Get Data Source](actions/get-data-source.md) | `GET v0/datasources/:name` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Get Environment Variable](actions/get-environment-variable.md) | `GET v0/variables/:name` | [docs](https://www.tinybird.co/docs/api-reference/environment-variables-api) |
| [Get Job](actions/get-job.md) | `GET v0/jobs/:id` | [docs](https://www.tinybird.co/docs/api-reference/jobs-api) |
| [Get Pipe](actions/get-pipe.md) | `GET v0/pipes/:name` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Get Static Token](actions/get-static-token.md) | `GET v0/tokens/:token` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
| [Ingest Events](actions/ingest-events.md) | `POST v0/events` | [docs](https://www.tinybird.co/docs/api-reference/events-api) |
| [List Data Sources](actions/list-data-sources.md) | `GET v0/datasources` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [List Environment Variables](actions/list-environment-variables.md) | `GET v0/variables` | [docs](https://www.tinybird.co/docs/api-reference/environment-variables-api) |
| [List Jobs](actions/list-jobs.md) | `GET v0/jobs` | [docs](https://www.tinybird.co/docs/api-reference/jobs-api) |
| [List Pipes](actions/list-pipes.md) | `GET v0/pipes` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [List Static Tokens](actions/list-static-tokens.md) | `GET v0/tokens` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
| [Query Pipe](actions/query-pipe.md) | `GET v0/pipes/:name.json` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Query Pipe (POST)](actions/query-pipe-post.md) | `POST v0/pipes/:name.json` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Refresh Static Token](actions/refresh-static-token.md) | `POST v0/tokens/:token/refresh` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
| [Replace Data](actions/replace-data.md) | `POST v0/datasources` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Truncate Data Source](actions/truncate-data-source.md) | `POST v0/datasources/:name/truncate` | [docs](https://www.tinybird.co/docs/api-reference/datasource-api) |
| [Update Environment Variable](actions/update-environment-variable.md) | `PUT v0/variables/:name` | [docs](https://www.tinybird.co/docs/api-reference/environment-variables-api) |
| [Update Pipe](actions/update-pipe.md) | `PUT v0/pipes/:name` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Update Pipe Node](actions/update-pipe-node.md) | `PUT v0/pipes/:name/nodes/:node` | [docs](https://www.tinybird.co/docs/api-reference/pipe-api) |
| [Update Static Token](actions/update-static-token.md) | `PUT v0/tokens/:token` | [docs](https://www.tinybird.co/docs/api-reference/token-api) |
