# List Calls with Synthflow AI Phone Calling

Retrieves all phone calls from Synthflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [List Calls](https://docs.synthflow.ai/api-reference/platform-api/calls/list-calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | How many calls to return per page. |
| `model_id` | query | `string` | yes | Return calls for the specified agent model ID. |
| `offset` | query | `number` | no | Index of the first call to return. |
