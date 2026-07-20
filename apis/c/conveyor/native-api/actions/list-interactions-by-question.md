# List Interactions By Question with Conveyor

Retrieves interactions for a knowledge base question from Conveyor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/interactions/questions/:question_id`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Interactions By Question](https://docs.conveyor.com/reference/get-interactions-by-question-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question_id` | path | `string` | yes | Knowledge base question identifier. |
| `created_at_start` | query | `date` | no | Start of created-at date range. |
| `created_at_end` | query | `date` | no | End of created-at date range. |
