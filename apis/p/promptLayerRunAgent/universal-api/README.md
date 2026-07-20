# <img src="https://images.mindcloud.co/apps/icons/promplaye_1777309577755.png" alt="PromptLayer Run Agent logo" width="28" height="28"> PromptLayer Run Agent: Universal API

Run and manage PromptLayer agents, workflows, and evaluations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/promptLayerRunAgent/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.promptlayer.com/
- **Vendor API docs:** https://docs.promptlayer.com/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new workflow in PromptLayer. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of workflows from PromptLayer. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing workflow in PromptLayer. |

### Agent Execution Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Execution Results](actions/get-agent-execution-results.md) | GET | Retrieves execution results for a PromptLayer workflow. |

### Agent Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Agent](actions/run-agent.md) | POST | Runs a PromptLayer workflow. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Version From File](actions/create-dataset-version-from-file.md) | POST | Creates a dataset version in PromptLayer from a file. |
| [Create Dataset Version From Request History](actions/create-dataset-version-from-request-history.md) | POST | Creates a dataset version in PromptLayer from request history. |
| [Get Dataset Rows](actions/get-dataset-rows.md) | GET | Retrieves rows from a PromptLayer dataset. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves a list of datasets from PromptLayer. |

### Dataset Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Group](actions/create-dataset-group.md) | POST | Creates a new dataset group in PromptLayer. |

### Evaluation

| Action | Method | Description |
| --- | --- | --- |
| [Get Evaluation](actions/get-evaluation.md) | GET | Retrieves a PromptLayer evaluation. |
| [Get Evaluation Rows](actions/get-evaluation-rows.md) | GET | Retrieves rows from a PromptLayer evaluation. |
| [Get Evaluation Score](actions/get-evaluation-score.md) | GET | Retrieves the score for a PromptLayer evaluation. |
| [List Evaluations](actions/list-evaluations.md) | GET | Retrieves evaluations from PromptLayer. |
| [Run Full Evaluation](actions/run-full-evaluation.md) | POST | Runs a full evaluation in PromptLayer. |

### Evaluation Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Add Column To Evaluation Pipeline](actions/add-column-to-evaluation-pipeline.md) | PUT | Adds a column to a PromptLayer evaluation pipeline. |
| [Configure Custom Scoring](actions/configure-custom-scoring.md) | PUT | Updates custom scoring for a PromptLayer evaluation. |
| [Create Evaluation Pipeline](actions/create-evaluation-pipeline.md) | POST | Creates a new evaluation pipeline in PromptLayer. |
| [Delete Evaluation Pipeline](actions/delete-evaluation-pipeline.md) | DELETE | Deletes a PromptLayer evaluation pipeline. |
| [Edit Evaluation Pipeline Column](actions/edit-evaluation-pipeline-column.md) | PUT | Updates a column in a PromptLayer evaluation pipeline. |
| [Rename Evaluation Pipeline](actions/rename-evaluation-pipeline.md) | PUT | Renames a PromptLayer evaluation pipeline. |

### Prompt Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Prompt Template](actions/get-prompt-template.md) | GET | Retrieves a prompt template from PromptLayer. |
| [Get Prompt Template Raw](actions/get-prompt-template-raw.md) | GET | Retrieves a raw prompt template from PromptLayer. |
| [List Prompt Templates](actions/list-prompt-templates.md) | GET | Retrieves prompt templates from PromptLayer. |
| [Patch Prompt Template Version](actions/patch-prompt-template-version.md) | PUT | Updates an existing prompt template version in PromptLayer. |
| [Publish Prompt Template](actions/publish-prompt-template.md) | POST | Publishes a prompt template in PromptLayer. |

### Prompt Template Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Track Prompt](actions/track-prompt.md) | PUT | Tracks prompts in PromptLayer. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Track Metadata](actions/track-metadata.md) | PUT | Tracks metadata in PromptLayer. |
| [Track Score](actions/track-score.md) | PUT | Tracks scores in PromptLayer. |

### Request Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Request](actions/get-request.md) | GET | Retrieves a request from PromptLayer. |
| [Log Request](actions/log-request.md) | POST | Logs a request in PromptLayer. |
| [Search Request Logs](actions/search-request-logs.md) | GET | Finds request logs in PromptLayer. |

### Skill Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Skill Collection](actions/create-skill-collection.md) | POST | Creates a new skill collection in PromptLayer. |
| [Get Skill Collection](actions/get-skill-collection.md) | GET | Retrieves a PromptLayer skill collection. |
| [List Skill Collections](actions/list-skill-collections.md) | GET | Retrieves skill collections from PromptLayer. |
| [Update Skill Collection](actions/update-skill-collection.md) | PUT | Updates an existing skill collection in PromptLayer. |

### Skill Collection Version

| Action | Method | Description |
| --- | --- | --- |
| [Save Skill Collection Version](actions/save-skill-collection-version.md) | POST | Creates a new PromptLayer skill collection version. |

### Span

| Action | Method | Description |
| --- | --- | --- |
| [Create Spans Bulk](actions/create-spans-bulk.md) | POST | Creates spans in bulk in PromptLayer. |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [Get Trace](actions/get-trace.md) | GET | Retrieves a trace from PromptLayer. |
| [Ingest Traces (OTLP)](actions/ingest-traces-otlp.md) | POST | Ingests trace data into PromptLayer using OTLP. |

