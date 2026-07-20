# Answer Query with Valyu

## Endpoint

- **Method:** `POST`
- **Path:** `/answer`
- **Base URL:** `https://api.valyu.ai/v1`
- **Official documentation:** [Answer Query](https://docs.valyu.ai/api-reference/endpoint/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The question or research query to answer. |
| `search_type` | body | `string` | no | Controls which data sources are searched for the answer. |
