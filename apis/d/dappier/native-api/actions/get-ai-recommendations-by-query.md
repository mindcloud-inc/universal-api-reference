# Get AI Recommendations By Query with Dappier

Retrieves AI article recommendations from Dappier by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/v2/search`
- **Base URL:** `https://api.dappier.com`
- **Official documentation:** [Get AI Recommendations By Query](https://docs.dappier.com/api-reference/endpoint/ai-recommendations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_model_id` | query | `string` | yes | Data model ID, starting with dm_. |
| `query` | body | `string` | yes | Natural language query, keyword, or URL. |
