# Create Evaluator with Arize AX

Creates a new evaluator in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/evaluators`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Create Evaluator](https://arize.com/docs/api-reference/evaluators/create-evaluator)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `version` | body | `object` | yes |
