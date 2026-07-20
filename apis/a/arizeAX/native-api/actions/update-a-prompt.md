# Update a Prompt with Arize AX

Updates a prompt in Arize AX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/prompts/:prompt_id`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Update a Prompt](https://arize.com/docs/api-reference/prompts/update-a-prompt)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `prompt_id` | path | `string` | yes |
