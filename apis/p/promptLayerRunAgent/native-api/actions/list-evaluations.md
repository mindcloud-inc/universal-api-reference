# List Evaluations with PromptLayer Run Agent

Retrieves evaluations from PromptLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/evaluations`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [List Evaluations](https://docs.promptlayer.com/reference/list-evaluations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Search for evaluations by name with a case-insensitive partial match. |
