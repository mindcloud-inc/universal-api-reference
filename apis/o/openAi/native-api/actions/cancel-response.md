# Cancel Response with Open AI

Cancels a model response in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/responses/:response_id/cancel`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Cancel Response](https://developers.openai.com/api/reference/resources/responses/methods/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | path | `string` | yes | The ID of the response to cancel. |
