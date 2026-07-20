# Create Evaluator Version with Arize AX

Creates a new evaluator version in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/evaluators/{evaluator_id}/versions`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Create Evaluator Version](https://arize.com/docs/api-reference/evaluators/create-evaluator-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commit_message` | body | `string` | yes |
| `evaluator_id` | path | `string` | yes |
| `template_config` | body | `object` | yes |
