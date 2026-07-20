# Get Domain-Constrained Recommendations with Dappier

Retrieves AI article recommendations from Dappier for a specified domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/v2/search`
- **Base URL:** `https://api.dappier.com`
- **Official documentation:** [Get Domain-Constrained Recommendations](https://docs.dappier.com/api-reference/endpoint/ai-recommendations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_model_id` | query | `string` | yes | Data model ID, starting with dm_. |
| `query` | body | `string` | yes | Natural language query, keyword, or URL. |
| `ref` | body | `string` | yes | The site domain where AI recommendations are being displayed. |
| `num_articles_ref` | body | `number` | yes | The minimum number of articles from the ref domain. |
