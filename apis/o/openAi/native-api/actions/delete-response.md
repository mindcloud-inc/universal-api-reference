# Delete Response with Open AI

Deletes a model response from Open AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/responses/:response_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Delete Response](https://developers.openai.com/api/reference/resources/responses/methods/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | path | `string` | yes | The ID of the response to delete. |
