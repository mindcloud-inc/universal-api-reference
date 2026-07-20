# Search with Valyu

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.valyu.ai/v1`
- **Official documentation:** [Search](https://docs.valyu.ai/api-reference/endpoint/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The search query to execute. |
| `max_num_results` | body | `number` | no | Maximum number of results to return. |
| `search_type` | body | `string` | no | Controls which data sources are searched. |
