# Arize AX: Native API Reference

A consolidated summary of Arize AX's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://arize.com/docs/ax/rest-reference/overview
- **OpenAPI specification:** https://api.arize.com/v2/spec.yaml
- **API base URL:** `https://api.arize.com`

## Authentication

### API Key

Connect Arize AX with a service key and the target Space ID for workspace-scoped REST API calls.

### Credentials

- **API Key:** `apiKey` · required
- **Space ID:** `spaceId` · required · The Arize AX workspace Space ID for workspace-scoped REST API calls.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://arize.com/docs/ax/reference/authentication-and-security/api-keys)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add New Examples To A Dataset](actions/add-new-examples-to-a-dataset.md) | `POST /v2/datasets/:dataset_id/examples` | [docs](https://arize.com/docs/api-reference/datasets/add-new-examples-to-a-dataset) |
| [Create a Dataset](actions/create-a-dataset.md) | `POST /v2/datasets` | [docs](https://arize.com/docs/api-reference/datasets/create-a-dataset) |
| [Create a Project](actions/create-a-project.md) | `POST /v2/projects` | [docs](https://arize.com/docs/api-reference/projects/create-a-project) |
| [Create a Prompt](actions/create-a-prompt.md) | `POST /v2/prompts` | [docs](https://arize.com/docs/api-reference/prompts/create-a-prompt) |
| [Create a Prompt Version](actions/create-a-prompt-version.md) | `POST /v2/prompts/:prompt_id/versions` | [docs](https://arize.com/docs/api-reference/prompts/create-a-prompt-version) |
| [Create an Experiment](actions/create-an-experiment.md) | `POST /v2/experiments` | [docs](https://arize.com/docs/api-reference/experiments/create-an-experiment) |
| [Create Evaluator](actions/create-evaluator.md) | `POST /v2/evaluators` | [docs](https://arize.com/docs/api-reference/evaluators/create-evaluator) |
| [Create Evaluator Version](actions/create-evaluator-version.md) | `POST /v2/evaluators/{evaluator_id}/versions` | [docs](https://arize.com/docs/api-reference/evaluators/create-evaluator-version) |
| [Get a Dataset](actions/get-a-dataset.md) | `GET /v2/datasets/:datasetId` | [docs](https://arize.com/docs/api-reference/datasets/get-a-dataset) |
| [Get a Project](actions/get-a-project.md) | `GET /v2/projects/:projectId` | [docs](https://arize.com/docs/api-reference/projects/get-a-project) |
| [Get a Prompt](actions/get-a-prompt.md) | `GET /v2/prompts/:promptId` | [docs](https://arize.com/docs/api-reference/prompts/get-a-prompt) |
| [Get a Prompt Version](actions/get-a-prompt-version.md) | `GET /v2/prompt-versions/:version_id` | [docs](https://arize.com/docs/api-reference/prompts/get-a-prompt-version) |
| [Get a Space](actions/get-a-space.md) | `GET /v2/spaces/:spaceId` | [docs](https://arize.com/docs/api-reference/spaces/get-a-space) |
| [Get an Experiment](actions/get-an-experiment.md) | `GET /v2/experiments/:experimentId` | [docs](https://arize.com/docs/api-reference/experiments/get-an-experiment) |
| [Get Evaluator](actions/get-evaluator.md) | `GET /v2/evaluators/:evaluatorId` | [docs](https://arize.com/docs/api-reference/evaluators/get-evaluator) |
| [Get Evaluator Version](actions/get-evaluator-version.md) | `GET /v2/evaluator-versions/:versionId` | [docs](https://arize.com/docs/api-reference/evaluators/get-evaluator-version) |
| [List Dataset Examples](actions/list-dataset-examples.md) | `GET /v2/datasets/:datasetId/examples` | [docs](https://arize.com/docs/api-reference/datasets/list-dataset-examples) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://arize.com/docs/api-reference/datasets/list-datasets) |
| [List Evaluator Versions](actions/list-evaluator-versions.md) | `GET /v2/evaluators/:evaluatorId/versions` | [docs](https://arize.com/docs/api-reference/evaluators/list-evaluator-versions) |
| [List Evaluators](actions/list-evaluators.md) | `GET /v2/evaluators` | [docs](https://arize.com/docs/api-reference/evaluators/list-evaluators) |
| [List Experiment Runs](actions/list-experiment-runs.md) | `GET /v2/experiments/:experimentId/runs` | [docs](https://arize.com/docs/api-reference/experiments/list-experiment-runs) |
| [List Experiments](actions/list-experiments.md) | `GET /v2/experiments` | [docs](https://arize.com/docs/api-reference/experiments/list-experiments) |
| [List Projects](actions/list-projects.md) | `GET /v2/projects` | [docs](https://arize.com/docs/api-reference/projects/list-projects) |
| [List Prompt Versions](actions/list-prompt-versions.md) | `GET /v2/prompts/:promptId/versions` | [docs](https://arize.com/docs/api-reference/prompts/list-prompt-versions) |
| [List Prompts](actions/list-prompts.md) | `GET /v2/prompts` | [docs](https://arize.com/docs/api-reference/prompts/list-prompts) |
| [List Spaces](actions/list-spaces.md) | `GET /v2/spaces` | [docs](https://arize.com/docs/api-reference/spaces/list-spaces) |
| [List Spans](actions/list-spans.md) | `POST /v2/spans` | [docs](https://arize.com/docs/api-reference/spans/list-spans) |
| [Update a Prompt](actions/update-a-prompt.md) | `PATCH /v2/prompts/:prompt_id` | [docs](https://arize.com/docs/api-reference/prompts/update-a-prompt) |
| [Update Evaluator](actions/update-evaluator.md) | `PATCH /v2/evaluators/{evaluator_id}` | [docs](https://arize.com/docs/api-reference/evaluators/update-evaluator) |
| [Update Existing Examples In A Dataset](actions/update-existing-examples-in-a-dataset.md) | `PATCH /v2/datasets/:dataset_id/examples` | [docs](https://arize.com/docs/api-reference/datasets/update-existing-examples-in-a-dataset) |
