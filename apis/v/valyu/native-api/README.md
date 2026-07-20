# Valyu: Native API Reference

A consolidated summary of Valyu's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.valyu.ai/home
- **API base URL:** `https://api.valyu.ai/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.valyu.ai/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer Query](actions/answer-query.md) | `POST /answer` | [docs](https://docs.valyu.ai/api-reference/endpoint/answer) |
| [Create Contents Job](actions/create-contents-job.md) | `POST /contents` | [docs](https://docs.valyu.ai/guides/content-extraction) |
| [Create DeepResearch Task](actions/create-deep-research-task.md) | `POST /deepresearch/tasks` | [docs](https://docs.valyu.ai/api-reference/endpoint/deepresearch-create) |
| [Extract Contents](actions/extract-contents.md) | `POST /contents` | [docs](https://docs.valyu.ai/api-reference/endpoint/contents) |
| [Get Contents Job Status](actions/get-contents-job-status.md) | `GET /contents/jobs/:job_id` | [docs](https://docs.valyu.ai/guides/content-extraction) |
| [Get DeepResearch Task Status](actions/get-deep-research-task-status.md) | `GET /deepresearch/tasks/:id/status` | [docs](https://docs.valyu.ai/api-reference/endpoint/deepresearch-status) |
| [List Datasource Categories](actions/list-datasource-categories.md) | `GET /datasources/categories` | [docs](https://docs.valyu.ai/api-reference/endpoint/datasources-categories) |
| [List Datasources](actions/list-datasources.md) | `GET /datasources` | [docs](https://docs.valyu.ai/api-reference/endpoint/datasources-list) |
| [List DeepResearch Tasks](actions/list-deep-research-tasks.md) | `GET /deepresearch/list` | [docs](https://docs.valyu.ai/api-reference/endpoint/deepresearch-list) |
| [Search](actions/search.md) | `POST /search` | [docs](https://docs.valyu.ai/api-reference/endpoint/search) |
| [Update DeepResearch Task](actions/update-deep-research-task.md) | `POST /deepresearch/tasks/:id/update` | [docs](https://docs.valyu.ai/api-reference/endpoint/deepresearch-update) |
