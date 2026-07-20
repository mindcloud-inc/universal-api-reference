# Search Real Time Data with Dappier

Retrieves a real-time AI search response from Dappier.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/aimodel/:aiModelId`
- **Base URL:** `https://api.dappier.com`
- **Official documentation:** [Search Real Time Data](https://docs.dappier.com/api-reference/endpoint/real-time-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aiModelId` | path | `string` | yes | The ID of the AI model to query. |
| `query` | body | `string` | yes | The query text to be passed to the AI model. |
