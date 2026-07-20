# Get Survey Responses with PickFu

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/[:id]/responses`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [Get Survey Responses](https://www.pickfu.com/docs/api-reference/responses/get-survey-responses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Survey GUID. |
| `question_id` | query | `string` | no | Filter responses to a specific question GUID. |
| `language` | query | `string` | no | Language code for response translations. |
