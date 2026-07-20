# <img src="https://images.mindcloud.co/apps/icons/images-6_1775150456343.png" alt="Keywords AI logo" width="28" height="28"> Keywords AI: Universal API

Respan provides an AI gateway plus prompts, datasets, evaluations, traces, and model management APIs for LLM applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keywordsAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://respan.ai
- **Vendor API docs:** https://www.respan.ai/docs/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Health Check](actions/health-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a dataset in Keywords AI. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves dataset records from Keywords AI. |

### Gateway

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Keywords AI. |
| [Create Response](actions/create-response.md) | POST | Creates a response in Keywords AI. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves the current API health status from Keywords AI. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Model](actions/create-custom-model.md) | POST | Creates or updates a custom model in Keywords AI. |
| [List Custom Models](actions/list-custom-models.md) | GET | Retrieves custom models from Keywords AI. |
| [List Models](actions/list-models.md) | GET | Retrieves public model catalog entries from Keywords AI. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a prompt in Keywords AI. |
| [Get Prompts Summary](actions/get-prompts-summary.md) | GET | Retrieves prompt summary statistics from Keywords AI. |
| [Get Prompts Summary With Filters](actions/get-prompts-summary-with-filters.md) | GET | Retrieves filtered prompt summary statistics from Keywords AI. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompt records from Keywords AI. |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Provider](actions/create-custom-provider.md) | POST | Creates a custom provider in Keywords AI. |
| [List Custom Providers](actions/list-custom-providers.md) | GET | Retrieves custom providers from Keywords AI. |

### Testset

| Action | Method | Description |
| --- | --- | --- |
| [Create Testset](actions/create-testset.md) | POST | Creates a testset in Keywords AI. |
| [List Testsets](actions/list-testsets.md) | GET | Retrieves testset records from Keywords AI. |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [List Traces](actions/list-traces.md) | GET | Retrieves trace records from Keywords AI. |

