# HoneyHive: Native API Reference

A consolidated summary of HoneyHive's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.honeyhive.ai/sdk-reference/authentication
- **OpenAPI specification:** https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml
- **API base URL:** `https://api.honeyhive.ai`

## Authentication

### API Key

Authenticate HoneyHive requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.honeyhive.ai/sdk-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Datapoints](actions/add-datapoints.md) | `POST /datasets/{dataset_id}/datapoints` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Configuration](actions/create-configuration.md) | `POST /configurations` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Datapoint](actions/create-datapoint.md) | `POST /datapoints` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Dataset](actions/create-dataset.md) | `POST /datasets` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Event Batch](actions/create-event-batch.md) | `POST /events/batch` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Metric](actions/create-metric.md) | `POST /metrics` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Model Event](actions/create-model-event.md) | `POST /events/model` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Model Event Batch](actions/create-model-event-batch.md) | `POST /events/model/batch` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Run](actions/create-run.md) | `POST /runs` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Create Tool](actions/create-tool.md) | `POST /tools` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Configuration](actions/delete-configuration.md) | `DELETE /configurations/{id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Datapoint](actions/delete-datapoint.md) | `DELETE /datapoints/{id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Dataset](actions/delete-dataset.md) | `DELETE /datasets` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Metric](actions/delete-metric.md) | `DELETE /metrics` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Run](actions/delete-run.md) | `DELETE /runs/{run_id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Delete Tool](actions/delete-tool.md) | `DELETE /tools` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Configurations](actions/get-configurations.md) | `GET /configurations` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Datapoint](actions/get-datapoint.md) | `GET /datapoints/{id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Datapoints](actions/get-datapoints.md) | `GET /datapoints` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Datasets](actions/get-datasets.md) | `GET /datasets` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Events](actions/get-events.md) | `POST /events/export` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Experiment Comparison](actions/get-experiment-comparison.md) | `GET /runs/{run_id_1}/compare-with/{run_id_2}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Experiment Result](actions/get-experiment-result.md) | `GET /runs/{run_id}/result` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Metrics](actions/get-metrics.md) | `GET /metrics` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Projects](actions/get-projects.md) | `GET /projects` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Run](actions/get-run.md) | `GET /runs/{run_id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Runs](actions/get-runs.md) | `GET /runs` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Session](actions/get-session.md) | `GET /session/{session_id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Get Tools](actions/get-tools.md) | `GET /tools` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Start Session](actions/start-session.md) | `POST /session/start` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Configuration](actions/update-configuration.md) | `PUT /configurations/{id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Datapoint](actions/update-datapoint.md) | `PUT /datapoints/{id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Dataset](actions/update-dataset.md) | `PUT /datasets` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Event](actions/update-event.md) | `PUT /events` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Metric](actions/update-metric.md) | `PUT /metrics` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Project](actions/update-project.md) | `PUT /projects` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Run](actions/update-run.md) | `PUT /runs/{run_id}` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
| [Update Tool](actions/update-tool.md) | `PUT /tools` | [docs](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml) |
