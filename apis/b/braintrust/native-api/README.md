# Braintrust: Native API Reference

A consolidated summary of Braintrust's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.braintrust.dev/docs/api-reference
- **OpenAPI specification:** https://raw.githubusercontent.com/braintrustdata/braintrust-openapi/main/openapi/spec.yaml
- **API base URL:** `https://api.braintrust.dev`

## Authentication

### API Key

Authenticate Braintrust requests with an API key or service token in the Authorization header.

### Credentials

- **API Key or Service Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.braintrust.dev/docs/core/organizations)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `objects`.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 0). Use `starting_after` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | `POST /v1/dataset` | [docs](https://www.braintrust.dev/docs/api-reference/datasets/create-dataset) |
| [Create Experiment](actions/create-experiment.md) | `POST /v1/experiment` | [docs](https://www.braintrust.dev/docs/api-reference/experiments/create-experiment) |
| [Create Function](actions/create-function.md) | `POST /v1/function` | [docs](https://braintrust.dev/docs/api-reference/functions/create-function.md) |
| [Create Project](actions/create-project.md) | `POST /v1/project` | [docs](https://www.braintrust.dev/docs/api-reference/projects/create-project) |
| [Create Project Score](actions/create-project-score.md) | `POST /v1/project_score` | [docs](https://www.braintrust.dev/docs/api-reference/project-scores/create-project-score) |
| [Create Project Tag](actions/create-project-tag.md) | `POST /v1/project_tag` | [docs](https://www.braintrust.dev/docs/api-reference/project-tags/create-project-tag) |
| [Create Prompt](actions/create-prompt.md) | `POST /v1/prompt` | [docs](https://www.braintrust.dev/docs/api-reference/prompts/create-prompt) |
| [Cross Object Insert](actions/cross-object-insert.md) | `POST /v1/insert` | [docs](https://braintrust.dev/docs/api-reference/crossobject/cross-object-insert.md) |
| [Feedback For Dataset Events](actions/feedback-for-dataset-events.md) | `POST /v1/dataset/:dataset_id/feedback` | [docs](https://braintrust.dev/docs/api-reference/datasets/feedback-for-dataset-events.md) |
| [Feedback For Experiment Events](actions/feedback-for-experiment-events.md) | `POST /v1/experiment/:experiment_id/feedback` | [docs](https://braintrust.dev/docs/api-reference/experiments/feedback-for-experiment-events.md) |
| [Feedback For Project Logs](actions/feedback-for-project-logs.md) | `POST /v1/project_logs/:project_id/feedback` | [docs](https://braintrust.dev/docs/api-reference/logs/feedback-for-project-logs-events.md) |
| [Fetch Dataset](actions/fetch-dataset.md) | `GET /v1/dataset/:dataset_id/fetch` | [docs](https://braintrust.dev/docs/api-reference/datasets/fetch-dataset-get-form.md) |
| [Fetch Experiment](actions/fetch-experiment.md) | `GET /v1/experiment/:experiment_id/fetch` | [docs](https://braintrust.dev/docs/api-reference/experiments/fetch-experiment-get-form.md) |
| [Fetch Project Logs](actions/fetch-project-logs.md) | `GET /v1/project_logs/:project_id/fetch` | [docs](https://braintrust.dev/docs/api-reference/logs/fetch-project-logs-get-form.md) |
| [Get Dataset](actions/get-dataset.md) | `GET /v1/dataset/:dataset_id` | [docs](https://braintrust.dev/docs/api-reference/datasets/get-dataset.md) |
| [Get Experiment](actions/get-experiment.md) | `GET /v1/experiment/:experiment_id` | [docs](https://braintrust.dev/docs/api-reference/experiments/get-experiment.md) |
| [Get Function](actions/get-function.md) | `GET /v1/function/:function_id` | [docs](https://braintrust.dev/docs/api-reference/functions/get-function.md) |
| [Get Organization](actions/get-organization.md) | `GET /v1/organization/:organization_id` | [docs](https://braintrust.dev/docs/api-reference/organizations/get-organization.md) |
| [Get Project](actions/get-project.md) | `GET /v1/project/:project_id` | [docs](https://braintrust.dev/docs/api-reference/projects/get-project.md) |
| [Get Prompt](actions/get-prompt.md) | `GET /v1/prompt/:prompt_id` | [docs](https://braintrust.dev/docs/api-reference/prompts/get-prompt.md) |
| [Insert Dataset Events](actions/insert-dataset-events.md) | `POST /v1/dataset/:dataset_id/insert` | [docs](https://braintrust.dev/docs/api-reference/datasets/insert-dataset-events.md) |
| [Insert Experiment Events](actions/insert-experiment-events.md) | `POST /v1/experiment/:experiment_id/insert` | [docs](https://braintrust.dev/docs/api-reference/experiments/insert-experiment-events.md) |
| [Insert Project Logs Events](actions/insert-project-logs-events.md) | `POST /v1/project_logs/:project_id/insert` | [docs](https://braintrust.dev/docs/api-reference/logs/insert-project-logs-events.md) |
| [Invoke Function](actions/invoke-function.md) | `POST /v1/function/:function_id/invoke` | [docs](https://braintrust.dev/docs/api-reference/functions/invoke-function.md) |
| [Launch Eval](actions/launch-eval.md) | `POST /v1/eval` | [docs](https://braintrust.dev/docs/api-reference/evals/launch-an-eval.md) |
| [List Datasets](actions/list-datasets.md) | `GET /v1/dataset` | [docs](https://braintrust.dev/docs/api-reference/datasets/list-datasets.md) |
| [List Experiments](actions/list-experiments.md) | `GET /v1/experiment` | [docs](https://braintrust.dev/docs/api-reference/experiments/list-experiments.md) |
| [List Functions](actions/list-functions.md) | `GET /v1/function` | [docs](https://braintrust.dev/docs/api-reference/functions/list-functions.md) |
| [List Organizations](actions/list-organizations.md) | `GET /v1/organization` | [docs](https://www.braintrust.dev/docs/api-reference/organizations/list-organizations) |
| [List Project Scores](actions/list-project-scores.md) | `GET /v1/project_score` | [docs](https://braintrust.dev/docs/api-reference/projectscores/list-project_scores.md) |
| [List Project Tags](actions/list-project-tags.md) | `GET /v1/project_tag` | [docs](https://braintrust.dev/docs/api-reference/projecttags/list-project_tags.md) |
| [List Projects](actions/list-projects.md) | `GET /v1/project` | [docs](https://braintrust.dev/docs/api-reference/projects/list-projects.md) |
| [List Prompts](actions/list-prompts.md) | `GET /v1/prompt` | [docs](https://braintrust.dev/docs/api-reference/prompts/list-prompts.md) |
| [List Users](actions/list-users.md) | `GET /v1/user` | [docs](https://braintrust.dev/docs/api-reference/users/list-users.md) |
| [List Views](actions/list-views.md) | `GET /v1/view` | [docs](https://braintrust.dev/docs/api-reference/views/list-views.md) |
| [Summarize Dataset](actions/summarize-dataset.md) | `GET /v1/dataset/:dataset_id/summarize` | [docs](https://braintrust.dev/docs/api-reference/datasets/summarize-dataset.md) |
| [Summarize Experiment](actions/summarize-experiment.md) | `GET /v1/experiment/:experiment_id/summarize` | [docs](https://braintrust.dev/docs/api-reference/experiments/summarize-experiment.md) |
| [Update Function](actions/update-function.md) | `PATCH /v1/function/:function_id` | [docs](https://braintrust.dev/docs/api-reference/functions/partially-update-function.md) |
| [Update Project](actions/update-project.md) | `PATCH /v1/project/:project_id` | [docs](https://braintrust.dev/docs/api-reference/projects/partially-update-project.md) |
| [Update Prompt](actions/update-prompt.md) | `PATCH /v1/prompt/:prompt_id` | [docs](https://braintrust.dev/docs/api-reference/prompts/partially-update-prompt.md) |
