# <img src="https://images.mindcloud.co/apps/icons/idq-p6wqff2-logos_1775069150591.jpeg" alt="LangChain logo" width="28" height="28"> LangChain: Universal API

LangSmith API by LangChain for traces, runs, datasets, experiments, feedback, and prompt repositories.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/langChain/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smith.langchain.com
- **Vendor API docs:** https://api.smith.langchain.com/redoc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sessions](actions/list-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST |  |
| [Get Dataset](actions/get-dataset.md) | GET |  |
| [List Datasets](actions/list-datasets.md) | GET |  |
| [Update Dataset](actions/update-dataset.md) | PUT |  |

### Example

| Action | Method | Description |
| --- | --- | --- |
| [Count Examples](actions/count-examples.md) | GET |  |
| [Create Example](actions/create-example.md) | POST |  |
| [Get Example](actions/get-example.md) | GET |  |
| [List Examples](actions/list-examples.md) | GET |  |
| [Update Example](actions/update-example.md) | PUT |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST |  |
| [Get Feedback](actions/get-feedback.md) | GET |  |
| [List Feedback](actions/list-feedback.md) | GET |  |
| [Update Feedback](actions/update-feedback.md) | PUT |  |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Run](actions/create-run.md) | POST |  |
| [Get Run](actions/get-run.md) | GET |  |
| [Get Run Stats](actions/get-run-stats.md) | GET |  |
| [Ingest Runs Batch](actions/ingest-runs-batch.md) | POST |  |
| [Query Runs](actions/query-runs.md) | GET |  |
| [Update Run](actions/update-run.md) | PUT |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [Get Session](actions/get-session.md) | GET |  |
| [Get Session Dashboard](actions/get-session-dashboard.md) | GET |  |
| [List Sessions](actions/list-sessions.md) | GET |  |
| [Update Session](actions/update-session.md) | PUT |  |

