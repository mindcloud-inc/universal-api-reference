# Update Prompt with Braintrust

Updates an existing prompt in Braintrust.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/prompt/:prompt_id`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Update Prompt](https://braintrust.dev/docs/api-reference/prompts/partially-update-prompt.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt_id` | path | `string` | yes | Prompt id. |
| `description` | body | `string` | no | Updated prompt description. |
