# List Evaluator Versions with Arize AX

Retrieves versions for an evaluator in Arize AX.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/evaluators/:evaluatorId/versions`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [List Evaluator Versions](https://arize.com/docs/api-reference/evaluators/list-evaluator-versions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `evaluator_id` | path | `string` | yes |
