# Get Evaluation Rows with PromptLayer Run Agent

Retrieves rows from a PromptLayer evaluation.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/evaluations/:evaluationId/rows`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Evaluation Rows](https://docs.promptlayer.com/reference/get-evaluation-rows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evaluationId` | path | `number` | yes | ID of the evaluation report to retrieve rows from. |
