# LangChain: Native API Reference

A consolidated summary of LangChain's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.smith.langchain.com/redoc
- **API base URL:** `https://api.smith.langchain.com`

## Authentication

### API Key

Authenticate with a LangSmith API key.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant ID:** `tenantId` · optional · Optional tenant/workspace identifier when required by your LangSmith setup.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.langchain.com/langsmith/create-account-api-key)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Examples](actions/count-examples.md) | `GET /api/v1/examples/count` | [docs](https://api.smith.langchain.com/redoc#tag/examples/operation/count_examples_api_v1_examples_count_get) |
| [Create Dataset](actions/create-dataset.md) | `POST /api/v1/datasets` | [docs](https://api.smith.langchain.com/redoc#tag/datasets/operation/create_dataset_api_v1_datasets_post) |
| [Create Example](actions/create-example.md) | `POST /api/v1/examples` | [docs](https://api.smith.langchain.com/redoc#tag/examples/operation/create_example_api_v1_examples_post) |
| [Create Feedback](actions/create-feedback.md) | `POST /api/v1/feedback` | [docs](https://api.smith.langchain.com/redoc#tag/feedback/operation/create_feedback_api_v1_feedback_post) |
| [Create Run](actions/create-run.md) | `POST /runs` | [docs](https://api.smith.langchain.com/redoc) |
| [Create Session](actions/create-session.md) | `POST /api/v1/sessions` | [docs](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/create_tracer_session_api_v1_sessions_post) |
| [Get Dataset](actions/get-dataset.md) | `GET /api/v1/datasets/:datasetId` | [docs](https://api.smith.langchain.com/redoc#tag/datasets/operation/read_dataset_api_v1_datasets__dataset_id__get) |
| [Get Example](actions/get-example.md) | `GET /api/v1/examples/:exampleId` | [docs](https://api.smith.langchain.com/redoc#tag/examples/operation/read_example_api_v1_examples__example_id__get) |
| [Get Feedback](actions/get-feedback.md) | `GET /api/v1/feedback/:feedbackId` | [docs](https://api.smith.langchain.com/redoc#tag/feedback/operation/read_feedback_api_v1_feedback__feedback_id__get) |
| [Get Run](actions/get-run.md) | `GET /api/v1/runs/:runId` | [docs](https://api.smith.langchain.com/redoc#tag/run/operation/read_run_api_v1_runs__run_id__get) |
| [Get Run Stats](actions/get-run-stats.md) | `POST /api/v1/runs/stats` | [docs](https://api.smith.langchain.com/redoc#tag/run/operation/stats_runs_api_v1_runs_stats_post) |
| [Get Session](actions/get-session.md) | `GET /api/v1/sessions/:sessionId` | [docs](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/read_tracer_session_api_v1_sessions__session_id__get) |
| [Get Session Dashboard](actions/get-session-dashboard.md) | `POST /api/v1/sessions/:sessionId/dashboard` | [docs](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/get_tracing_project_prebuilt_dashboard_api_v1_sessions__session_id__dashboard_post) |
| [Ingest Runs Batch](actions/ingest-runs-batch.md) | `POST /runs/batch` | [docs](https://api.smith.langchain.com/redoc) |
| [List Datasets](actions/list-datasets.md) | `GET /api/v1/datasets` | [docs](https://api.smith.langchain.com/redoc#tag/datasets/operation/read_datasets_api_v1_datasets_get) |
| [List Examples](actions/list-examples.md) | `GET /api/v1/examples` | [docs](https://api.smith.langchain.com/redoc#tag/examples/operation/read_examples_api_v1_examples_get) |
| [List Feedback](actions/list-feedback.md) | `GET /api/v1/feedback` | [docs](https://api.smith.langchain.com/redoc#tag/feedback/operation/read_feedbacks_api_v1_feedback_get) |
| [List Sessions](actions/list-sessions.md) | `GET /api/v1/sessions` | [docs](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/read_tracer_sessions_api_v1_sessions_get) |
| [Query Runs](actions/query-runs.md) | `POST /api/v1/runs/query` | [docs](https://api.smith.langchain.com/redoc#tag/run/operation/query_runs_api_v1_runs_query_post) |
| [Update Dataset](actions/update-dataset.md) | `PATCH /api/v1/datasets/:datasetId` | [docs](https://api.smith.langchain.com/redoc#tag/datasets/operation/update_dataset_api_v1_datasets__dataset_id__patch) |
| [Update Example](actions/update-example.md) | `PATCH /api/v1/examples/:exampleId` | [docs](https://api.smith.langchain.com/redoc#tag/examples/operation/update_example_api_v1_examples__example_id__patch) |
| [Update Feedback](actions/update-feedback.md) | `PATCH /api/v1/feedback/:feedbackId` | [docs](https://api.smith.langchain.com/redoc#tag/feedback/operation/update_feedback_api_v1_feedback__feedback_id__patch) |
| [Update Run](actions/update-run.md) | `PATCH /api/v1/runs/:runId` | [docs](https://api.smith.langchain.com/redoc#tag/run/operation/update_run_api_v1_runs__run_id__patch) |
| [Update Session](actions/update-session.md) | `PATCH /api/v1/sessions/:sessionId` | [docs](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/update_tracer_session_api_v1_sessions__session_id__patch) |
