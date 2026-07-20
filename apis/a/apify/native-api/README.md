# Apify: Native API Reference

A consolidated summary of Apify's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.apify.com/api/v2
- **OpenAPI specification:** https://docs.apify.com/api/openapi.json
- **API base URL:** `https://api.apify.com`

## Authentication

### API token

Use an Apify API token. Apify recommends sending it in the Authorization header as Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.apify.com/api/v2#authentication)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sortBy` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 4 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Limits](actions/get-account-limits.md) | `GET /v2/users/me/limits` | [docs](https://docs.apify.com/api/v2/users-me-limits-get) |
| [Get Actor](actions/get-actor.md) | `GET /v2/acts/:actorId` | [docs](https://docs.apify.com/api/v2/act-get) |
| [Get Actor Build](actions/get-actor-build.md) | `GET /v2/acts/:actorId/builds/:buildId` | [docs](https://docs.apify.com/api/v2/act-build-get) |
| [Get Actor Run](actions/get-actor-run.md) | `GET /v2/acts/:actorId/runs/:runId` | [docs](https://docs.apify.com/api/v2/act-run-get) |
| [Get Actor Task](actions/get-actor-task.md) | `GET /v2/actor-tasks/:actorTaskId` | [docs](https://docs.apify.com/api/v2/actor-task-get) |
| [Get Actor Task Input](actions/get-actor-task-input.md) | `GET /v2/actor-tasks/:actorTaskId/input` | [docs](https://docs.apify.com/api/v2/actor-task-input-get) |
| [Get Dataset](actions/get-dataset.md) | `GET /v2/datasets/:datasetId` | [docs](https://docs.apify.com/api/v2/dataset-get) |
| [Get Dataset Items](actions/get-dataset-items.md) | `GET /v2/datasets/:datasetId/items` | [docs](https://docs.apify.com/api/v2/dataset-items-get) |
| [Get Dataset Statistics](actions/get-dataset-statistics.md) | `GET /v2/datasets/:datasetId/statistics` | [docs](https://docs.apify.com/api/v2/dataset-statistics-get) |
| [Get Key-Value Store](actions/get-key-value-store.md) | `GET /v2/key-value-stores/:storeId` | [docs](https://docs.apify.com/api/v2/key-value-store-get) |
| [Get Last Actor Run](actions/get-last-actor-run.md) | `GET /v2/acts/:actorId/runs/last` | [docs](https://docs.apify.com/api/v2/act-runs-last-get) |
| [Get Last Actor Task Run](actions/get-last-actor-task-run.md) | `GET /v2/actor-tasks/:actorTaskId/runs/last` | [docs](https://docs.apify.com/api/v2/actor-task-runs-last-get) |
| [Get Monthly Usage](actions/get-monthly-usage.md) | `GET /v2/users/me/usage/monthly` | [docs](https://docs.apify.com/api/v2/users-me-usage-monthly-get) |
| [Get Private User Data](actions/get-private-user-data.md) | `GET /v2/users/me` | [docs](https://docs.apify.com/api/v2/users-me-get) |
| [Get Request Queue](actions/get-request-queue.md) | `GET /v2/request-queues/:queueId` | [docs](https://docs.apify.com/api/v2/request-queue-get) |
| [List Actor Builds](actions/list-actor-builds.md) | `GET /v2/acts/:actorId/builds` | [docs](https://docs.apify.com/api/v2/act-builds-get) |
| [List Actor Runs](actions/list-actor-runs.md) | `GET /v2/acts/:actorId/runs` | [docs](https://docs.apify.com/api/v2/act-runs-get) |
| [List Actor Task Runs](actions/list-actor-task-runs.md) | `GET /v2/actor-tasks/:actorTaskId/runs` | [docs](https://docs.apify.com/api/v2/actor-task-runs-get) |
| [List Actor Tasks](actions/list-actor-tasks.md) | `GET /v2/actor-tasks` | [docs](https://docs.apify.com/api/v2/actor-tasks-get) |
| [List Actor Versions](actions/list-actor-versions.md) | `GET /v2/acts/:actorId/versions` | [docs](https://docs.apify.com/api/v2/act-versions-get) |
| [List Actors](actions/list-actors.md) | `GET /v2/acts` | [docs](https://docs.apify.com/api/v2/acts-get) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://docs.apify.com/api/v2/datasets-get) |
| [List Key-Value Stores](actions/list-key-value-stores.md) | `GET /v2/key-value-stores` | [docs](https://docs.apify.com/api/v2/key-value-stores-get) |
| [List Request Queues](actions/list-request-queues.md) | `GET /v2/request-queues` | [docs](https://docs.apify.com/api/v2/request-queues-get) |
