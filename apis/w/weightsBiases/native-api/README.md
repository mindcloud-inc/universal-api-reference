# Weights & Biases: Native API Reference

A consolidated summary of Weights & Biases's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.wandb.ai/weave/reference/service-api
- **API base URL:** `https://trace.wandb.ai`

## Authentication

### W&B API Key

Authenticate with a W&B API key. Protected Weave Service API requests are sent using Basic authentication with username `api` and the API key as the password.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.wandb.ai/weave/reference/service-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Call Stats](actions/get-call-stats.md) | `POST /calls/stats` | [docs](https://docs.wandb.ai/weave/reference/service-api/calls/call-stats) |
| [Get Caller Location](actions/get-caller-location.md) | `GET /geolocate` | [docs](https://docs.wandb.ai/weave/reference/service-api/service/get-caller-location) |
| [Get Calls Count](actions/get-calls-count.md) | `POST /calls/query_stats` | [docs](https://docs.wandb.ai/weave/reference/service-api/calls/calls-query-stats) |
| [Get Calls Usage](actions/get-calls-usage.md) | `POST /calls/usage` | [docs](https://docs.wandb.ai/weave/reference/service-api/calls/calls-usage) |
| [Get Feedback Payload Schema](actions/get-feedback-payload-schema.md) | `POST /feedback/payload_schema` | [docs](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-payload-schema) |
| [Get Feedback Stats](actions/get-feedback-stats.md) | `POST /feedback/stats` | [docs](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-stats) |
| [Get File Content](actions/get-file-content.md) | `POST /file/content` | [docs](https://docs.wandb.ai/weave/reference/service-api/files/file-content) |
| [Get Files Stats](actions/get-files-stats.md) | `POST /files/query_stats` | [docs](https://docs.wandb.ai/weave/reference/service-api/files/files-stats) |
| [Get Projects Info](actions/get-projects-info.md) | `POST /service/projects_info` | [docs](https://docs.wandb.ai/weave/reference/service-api/service/projects-info) |
| [Get Server Info](actions/get-server-info.md) | `GET /server_info` | [docs](https://docs.wandb.ai/weave/reference/service-api/service/server-info) |
| [Get Table Stats](actions/get-table-stats.md) | `POST /table/query_stats` | [docs](https://docs.wandb.ai/weave/reference/service-api/tables/table-query-stats) |
| [List Aliases](actions/list-aliases.md) | `GET /aliases` | [docs](https://docs.wandb.ai/weave/reference/service-api/objects/aliases-list) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://docs.wandb.ai/weave/reference/service-api/objects/tags-list) |
| [Query Calls](actions/query-calls.md) | `POST /calls/stream_query` | [docs](https://docs.wandb.ai/weave/reference/service-api/calls/calls-query-stream) |
| [Query Costs](actions/query-costs.md) | `POST /cost/query` | [docs](https://docs.wandb.ai/weave/reference/service-api/costs/cost-query) |
| [Query Feedback](actions/query-feedback.md) | `POST /feedback/query` | [docs](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-query) |
| [Query Objects](actions/query-objects.md) | `POST /objs/query` | [docs](https://docs.wandb.ai/weave/reference/service-api/objects/objs-query) |
| [Query Table](actions/query-table.md) | `POST /table/query` | [docs](https://docs.wandb.ai/weave/reference/service-api/tables/table-query) |
| [Query Threads](actions/query-threads.md) | `POST /threads/stream_query` | [docs](https://docs.wandb.ai/weave/reference/service-api/threads/threads-query-stream) |
| [Read Call](actions/read-call.md) | `POST /call/read` | [docs](https://docs.wandb.ai/weave/reference/service-api/calls/call-read) |
| [Read Object](actions/read-object.md) | `POST /obj/read` | [docs](https://docs.wandb.ai/weave/reference/service-api/objects/obj-read) |
| [Read Refs Batch](actions/read-refs-batch.md) | `POST /refs/read_batch` | [docs](https://docs.wandb.ai/weave/reference/service-api/refs/refs-read-batch) |
| [Read Root](actions/read-root.md) | `GET /health` | [docs](https://docs.wandb.ai/weave/reference/service-api/service/read-root) |
| [Read Version](actions/read-version.md) | `GET /version` | [docs](https://docs.wandb.ai/weave/reference/service-api/service/read-version) |
