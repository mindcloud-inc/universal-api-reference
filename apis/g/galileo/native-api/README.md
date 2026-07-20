# Galileo: Native API Reference

A consolidated summary of Galileo's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.galileo.ai/api-reference
- **OpenAPI specification:** https://api.galileo.ai/public/v2/openapi.json
- **API base URL:** `https://api.galileo.ai`

## Authentication

### Galileo API Key

Authenticate Galileo REST requests with the provider-native API key in the Galileo-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.galileo.ai/api-reference/auth/login-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `starting_token` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Collaborator Roles](actions/get-collaborator-roles.md) | `GET /v2/collaborator_roles` | [docs](https://docs.galileo.ai/api-reference/projects/get-collaborator-roles) |
| [Get Current User](actions/get-current-user.md) | `GET /v2/current_user` | [docs](https://docs.galileo.ai/api-reference/users/current-user) |
| [Get Dataset](actions/get-dataset.md) | `GET /v2/datasets/:dataset_id` | [docs](https://docs.galileo.ai/api-reference/datasets/get-dataset) |
| [Get Dataset Content](actions/get-dataset-content.md) | `GET /v2/datasets/:dataset_id/content` | [docs](https://docs.galileo.ai/api-reference/datasets/get-dataset-content) |
| [Get Experiment](actions/get-experiment.md) | `GET /v2/projects/:project_id/experiments/:experiment_id` | [docs](https://docs.galileo.ai/api-reference/experiment/get-experiment) |
| [Get Experiment Metric Settings](actions/get-experiment-metric-settings.md) | `GET /v2/projects/:project_id/experiments/:experiment_id/metric_settings` | [docs](https://docs.galileo.ai/api-reference/experiment/get-metric-settings) |
| [Get Experiment Metrics](actions/get-experiment-metrics.md) | `POST /v2/projects/:project_id/experiments/:experiment_id/metrics` | [docs](https://docs.galileo.ai/api-reference/trends-dashboard/get-experiment-metrics) |
| [Get Integration](actions/get-integration.md) | `GET /v2/integrations/:name` | [docs](https://docs.galileo.ai/api-reference/integrations/get-integration) |
| [Get Integration Status](actions/get-integration-status.md) | `GET /v2/integrations/:name/status` | [docs](https://docs.galileo.ai/api-reference/integrations/get-integration-status) |
| [Get Log Stream](actions/get-log-stream.md) | `GET /v2/projects/:project_id/log_streams/:log_stream_id` | [docs](https://docs.galileo.ai/api-reference/log-stream/get-log-stream) |
| [Get Log Stream Metric Settings](actions/get-log-stream-metric-settings.md) | `GET /v2/projects/:project_id/log_streams/:log_stream_id/metric_settings` | [docs](https://docs.galileo.ai/api-reference/log-stream/get-metric-settings) |
| [Get Project](actions/get-project.md) | `GET /v2/projects/:project_id` | [docs](https://docs.galileo.ai/api-reference/projects/get-project) |
| [Get Project Alert](actions/get-project-alert.md) | `GET /v2/projects/:project_id/alerts/:monitor_alert_config_id` | [docs](https://docs.galileo.ai/api-reference/log-stream-alerts/get-alert-by-id) |
| [Get Span](actions/get-span.md) | `GET /v2/projects/:project_id/spans/:span_id` | [docs](https://docs.galileo.ai/api-reference/trace/get-span) |
| [Get Trace](actions/get-trace.md) | `GET /v2/projects/:project_id/traces/:trace_id` | [docs](https://docs.galileo.ai/api-reference/trace/get-trace) |
| [Healthcheck](actions/healthcheck.md) | `GET /v2/healthcheck` | [docs](https://docs.galileo.ai/api-reference/health/healthcheck) |
| [List Available Integrations](actions/list-available-integrations.md) | `GET /v2/integrations/available` | [docs](https://docs.galileo.ai/api-reference/integrations/list-available-integrations) |
| [List Current User Groups](actions/list-current-user-groups.md) | `GET /v2/current_user/groups` | [docs](https://docs.galileo.ai/api-reference/groups/list-current-user-groups) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://docs.galileo.ai/api-reference/datasets/list-datasets) |
| [List Experiments](actions/list-experiments.md) | `GET /v2/projects/:project_id/experiments` | [docs](https://docs.galileo.ai/api-reference/experiment/list-experiments) |
| [List Experiments Paginated](actions/list-experiments-paginated.md) | `GET /v2/projects/:project_id/experiments/paginated` | [docs](https://docs.galileo.ai/api-reference/experiment/list-experiments-paginated) |
| [List Log Streams](actions/list-log-streams.md) | `GET /v2/projects/:project_id/log_streams` | [docs](https://docs.galileo.ai/api-reference/log-stream/list-log-streams) |
| [List Log Streams Paginated](actions/list-log-streams-paginated.md) | `GET /v2/projects/:project_id/log_streams/paginated` | [docs](https://docs.galileo.ai/api-reference/log-stream/list-log-streams-paginated) |
| [List Project Alerts](actions/list-project-alerts.md) | `GET /v2/projects/:project_id/alerts` | [docs](https://docs.galileo.ai/api-reference/log-stream-alerts/list-alerts-by-project) |
| [List Project Groups](actions/list-project-groups.md) | `GET /v2/projects/:project_id/groups` | [docs](https://docs.galileo.ai/api-reference/projects/list-group-project-collaborators) |
| [List Project Users](actions/list-project-users.md) | `GET /v2/projects/:project_id/users` | [docs](https://docs.galileo.ai/api-reference/projects/list-user-project-collaborators) |
| [List Projects](actions/list-projects.md) | `POST /v2/projects/paginated` | [docs](https://docs.galileo.ai/api-reference/projects/get-projects-v2) |
| [Query Dataset Content](actions/query-dataset-content.md) | `POST /v2/datasets/:dataset_id/content/query` | [docs](https://docs.galileo.ai/api-reference/datasets/query-dataset-content) |
| [Query Dataset Versions](actions/query-dataset-versions.md) | `POST /v2/datasets/:dataset_id/versions/query` | [docs](https://docs.galileo.ai/api-reference/datasets/query-dataset-versions) |
| [Query Datasets](actions/query-datasets.md) | `POST /v2/datasets/query` | [docs](https://docs.galileo.ai/api-reference/datasets/query-datasets) |
| [Query Spans](actions/query-spans.md) | `POST /v2/projects/:project_id/spans/search` | [docs](https://docs.galileo.ai/api-reference/trace/query-spans) |
| [Query Traces](actions/query-traces.md) | `POST /v2/projects/:project_id/traces/search` | [docs](https://docs.galileo.ai/api-reference/trace/query-traces) |
| [Search Experiments](actions/search-experiments.md) | `POST /v2/projects/:project_id/experiments/search` | [docs](https://docs.galileo.ai/api-reference/experiment/search-experiments) |
| [Search Log Streams](actions/search-log-streams.md) | `POST /v2/projects/:project_id/log_streams/search` | [docs](https://docs.galileo.ai/api-reference/log-stream/search-log-streams) |
