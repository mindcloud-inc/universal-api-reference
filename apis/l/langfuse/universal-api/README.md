# <img src="https://images.mindcloud.co/apps/icons/images_1775833649424.jpeg" alt="Langfuse logo" width="28" height="28"> Langfuse: Universal API

Observe LLM traces, manage prompts, run evaluations, and analyze metrics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/langfuse/latest
- **Category:** IT Operations / Observability
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://langfuse.com
- **Vendor API docs:** https://langfuse.com/docs/api-and-data-platform/features/public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project](actions/get-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Annotation Queue

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation Queue](actions/create-annotation-queue.md) | POST | Creates an annotation queue in Langfuse. |
| [Get Annotation Queue](actions/get-annotation-queue.md) | GET | Retrieves an annotation queue from Langfuse. |
| [List Annotation Queues](actions/list-annotation-queues.md) | GET | Retrieves annotation queues from Langfuse. |

### Annotation Queue Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation Queue Item](actions/create-annotation-queue-item.md) | POST | Adds an item to a Langfuse annotation queue. |
| [Get Annotation Queue Item](actions/get-annotation-queue-item.md) | GET | Retrieves an item from a Langfuse annotation queue. |
| [List Annotation Queue Items](actions/list-annotation-queue-items.md) | GET | Retrieves items from a Langfuse annotation queue. |
| [Update Annotation Queue Item](actions/update-annotation-queue-item.md) | PUT | Updates an item in a Langfuse annotation queue. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment in Langfuse. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Langfuse. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a dataset in Langfuse. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Langfuse. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Langfuse. |

### Dataset Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Item](actions/create-dataset-item.md) | POST | Creates a dataset item in Langfuse. |
| [Get Dataset Item](actions/get-dataset-item.md) | GET | Retrieves a dataset item from Langfuse. |
| [List Dataset Items](actions/list-dataset-items.md) | GET | Retrieves dataset items from Langfuse. |

### Dataset Run

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Runs](actions/list-dataset-runs.md) | GET | Retrieves dataset runs from Langfuse. |

### Dataset Run Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Run Item](actions/create-dataset-run-item.md) | POST | Creates a dataset run item in Langfuse. |
| [List Dataset Run Items](actions/list-dataset-run-items.md) | GET | Retrieves dataset run items from Langfuse. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Query Metrics](actions/query-metrics.md) | GET | Retrieves project metrics from Langfuse. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from Langfuse. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Langfuse. |

### Observation

| Action | Method | Description |
| --- | --- | --- |
| [List Observations](actions/list-observations.md) | GET | Retrieves observations from Langfuse. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves the project associated with your Langfuse API key. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a new prompt version in Langfuse. |
| [Delete Prompt](actions/delete-prompt.md) | DELETE | Deletes prompt versions from Langfuse. |
| [Get Prompt](actions/get-prompt.md) | GET | Retrieves a prompt from Langfuse. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from Langfuse. |

### Prompt Version

| Action | Method | Description |
| --- | --- | --- |
| [Update Prompt Version](actions/update-prompt-version.md) | PUT | Updates labels for a Langfuse prompt version. |

### Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Score](actions/get-score.md) | GET | Retrieves a score from Langfuse. |
| [List Scores](actions/list-scores.md) | GET | Retrieves scores from Langfuse. |

### Score Config

| Action | Method | Description |
| --- | --- | --- |
| [Create Score Config](actions/create-score-config.md) | POST | Creates a score config in Langfuse. |
| [Get Score Config](actions/get-score-config.md) | GET | Retrieves a score config from Langfuse. |
| [List Score Configs](actions/list-score-configs.md) | GET | Retrieves score configs from Langfuse. |
| [Update Score Config](actions/update-score-config.md) | PUT | Updates an existing score config in Langfuse. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Langfuse. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Langfuse. |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [Delete Trace](actions/delete-trace.md) | DELETE | Deletes a trace from Langfuse. |
| [Delete Traces](actions/delete-traces.md) | DELETE | Deletes multiple traces from Langfuse. |
| [Get Trace](actions/get-trace.md) | GET | Retrieves a trace from Langfuse. |
| [List Traces](actions/list-traces.md) | GET | Retrieves traces from Langfuse. |

