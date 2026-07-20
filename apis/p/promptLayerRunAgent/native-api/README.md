# PromptLayer Run Agent: Native API Reference

A consolidated summary of PromptLayer Run Agent's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.promptlayer.com/reference/introduction
- **API base URL:** `https://api.promptlayer.com`

## Authentication

### API Key

Connect PromptLayer with a workspace API key.

### Credentials

- **API Key:** `apiKey` · required · PromptLayer workspace API key.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.promptlayer.com/reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Column To Evaluation Pipeline](actions/add-column-to-evaluation-pipeline.md) | `POST /report-columns` | [docs](https://docs.promptlayer.com/reference/add-report-columns) |
| [Configure Custom Scoring](actions/configure-custom-scoring.md) | `PATCH /reports/:reportId/score-card` | [docs](https://docs.promptlayer.com/reference/update-report-score-card) |
| [Create Agent](actions/create-agent.md) | `POST /rest/workflows` | [docs](https://docs.promptlayer.com/reference/create-workflow) |
| [Create Dataset Group](actions/create-dataset-group.md) | `POST /api/public/v2/dataset-groups` | [docs](https://docs.promptlayer.com/reference/create-dataset-group) |
| [Create Dataset Version From File](actions/create-dataset-version-from-file.md) | `POST /api/public/v2/dataset-versions/from-file` | [docs](https://docs.promptlayer.com/reference/create-dataset-version-from-file) |
| [Create Dataset Version From Request History](actions/create-dataset-version-from-request-history.md) | `POST /api/public/v2/dataset-versions/from-filter-params` | [docs](https://docs.promptlayer.com/reference/create-dataset-version-from-filter-params) |
| [Create Evaluation Pipeline](actions/create-evaluation-pipeline.md) | `POST /reports` | [docs](https://docs.promptlayer.com/reference/create-reports) |
| [Create Skill Collection](actions/create-skill-collection.md) | `POST /api/public/v2/skill-collections` | [docs](https://docs.promptlayer.com/reference/create-skill-collection) |
| [Create Spans Bulk](actions/create-spans-bulk.md) | `POST /spans-bulk` | [docs](https://docs.promptlayer.com/reference/spans-bulk) |
| [Delete Evaluation Pipeline](actions/delete-evaluation-pipeline.md) | `DELETE /reports/:reportId` | [docs](https://docs.promptlayer.com/reference/delete-report) |
| [Edit Evaluation Pipeline Column](actions/edit-evaluation-pipeline-column.md) | `PATCH /report-columns/:reportColumnId` | [docs](https://docs.promptlayer.com/reference/edit-report-column) |
| [Get Agent Execution Results](actions/get-agent-execution-results.md) | `GET /workflow-version-execution-results` | [docs](https://docs.promptlayer.com/reference/workflow-version-execution-results) |
| [Get Dataset Rows](actions/get-dataset-rows.md) | `GET /api/public/v2/datasets/:datasetId/rows` | [docs](https://docs.promptlayer.com/reference/get-dataset-rows) |
| [Get Evaluation](actions/get-evaluation.md) | `GET /reports/:reportId` | [docs](https://docs.promptlayer.com/reference/get-report) |
| [Get Evaluation Rows](actions/get-evaluation-rows.md) | `GET /api/public/v2/evaluations/:evaluationId/rows` | [docs](https://docs.promptlayer.com/reference/get-evaluation-rows) |
| [Get Evaluation Score](actions/get-evaluation-score.md) | `GET /reports/:reportId/score` | [docs](https://docs.promptlayer.com/reference/get-report-score) |
| [Get Prompt Template](actions/get-prompt-template.md) | `POST /prompt-templates/:identifier` | [docs](https://docs.promptlayer.com/reference/templates-get) |
| [Get Prompt Template Raw](actions/get-prompt-template-raw.md) | `GET /prompt-templates/:identifier` | [docs](https://docs.promptlayer.com/reference/templates-get-raw) |
| [Get Request](actions/get-request.md) | `GET /api/public/v2/requests/:request_id` | [docs](https://docs.promptlayer.com/reference/get-request) |
| [Get Skill Collection](actions/get-skill-collection.md) | `GET /api/public/v2/skill-collections/:identifier` | [docs](https://docs.promptlayer.com/reference/get-skill-collection) |
| [Get Trace](actions/get-trace.md) | `GET /api/public/v2/traces/:trace_id` | [docs](https://docs.promptlayer.com/reference/get-trace) |
| [Ingest Traces (OTLP)](actions/ingest-traces-otlp.md) | `POST /v1/traces` | [docs](https://docs.promptlayer.com/reference/otlp-ingest-traces) |
| [List Agents](actions/list-agents.md) | `GET /workflows` | [docs](https://docs.promptlayer.com/reference/list-workflows) |
| [List Datasets](actions/list-datasets.md) | `GET /api/public/v2/datasets` | [docs](https://docs.promptlayer.com/reference/list-datasets) |
| [List Evaluations](actions/list-evaluations.md) | `GET /api/public/v2/evaluations` | [docs](https://docs.promptlayer.com/reference/list-evaluations) |
| [List Prompt Templates](actions/list-prompt-templates.md) | `GET /prompt-templates` | [docs](https://docs.promptlayer.com/reference/list-prompt-templates) |
| [List Skill Collections](actions/list-skill-collections.md) | `GET /api/public/v2/skill-collections` | [docs](https://docs.promptlayer.com/reference/list-skill-collections) |
| [Log Request](actions/log-request.md) | `POST /log-request` | [docs](https://docs.promptlayer.com/reference/log-request) |
| [Patch Prompt Template Version](actions/patch-prompt-template-version.md) | `PATCH /rest/prompt-templates/:identifier` | [docs](https://docs.promptlayer.com/reference/templates-patch) |
| [Publish Prompt Template](actions/publish-prompt-template.md) | `POST /rest/prompt-templates` | [docs](https://docs.promptlayer.com/reference/templates-publish) |
| [Rename Evaluation Pipeline](actions/rename-evaluation-pipeline.md) | `PATCH /reports/:reportId/rename` | [docs](https://docs.promptlayer.com/reference/rename-report) |
| [Run Agent](actions/run-agent.md) | `POST /workflows/:workflow_name/run` | [docs](https://docs.promptlayer.com/reference/run-workflow) |
| [Run Full Evaluation](actions/run-full-evaluation.md) | `POST /reports/:reportId/run` | [docs](https://docs.promptlayer.com/reference/run-report) |
| [Save Skill Collection Version](actions/save-skill-collection-version.md) | `POST /api/public/v2/skill-collections/:identifier/versions` | [docs](https://docs.promptlayer.com/reference/save-skill-collection-version) |
| [Search Request Logs](actions/search-request-logs.md) | `POST /api/public/v2/requests/search` | [docs](https://docs.promptlayer.com/reference/search-request-logs) |
| [Track Metadata](actions/track-metadata.md) | `POST /rest/track-metadata` | [docs](https://docs.promptlayer.com/reference/track-metadata) |
| [Track Prompt](actions/track-prompt.md) | `POST /rest/track-prompt` | [docs](https://docs.promptlayer.com/reference/track-prompt) |
| [Track Score](actions/track-score.md) | `POST /rest/track-score` | [docs](https://docs.promptlayer.com/reference/track-score) |
| [Update Agent](actions/update-agent.md) | `PATCH /rest/workflows/:workflow_id_or_name` | [docs](https://docs.promptlayer.com/reference/patch-workflow) |
| [Update Skill Collection](actions/update-skill-collection.md) | `PATCH /api/public/v2/skill-collections/:identifier` | [docs](https://docs.promptlayer.com/reference/update-skill-collection) |
