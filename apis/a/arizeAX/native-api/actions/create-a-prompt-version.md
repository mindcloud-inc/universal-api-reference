# Create a Prompt Version with Arize AX

Creates a new prompt version in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/prompts/:prompt_id/versions`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Create a Prompt Version](https://arize.com/docs/api-reference/prompts/create-a-prompt-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commit_message` | body | `string` | yes |
| `input_variable_format` | body | `string` | yes |
| `messages[]` | body | `array<object>` | yes |
| `prompt_id` | path | `string` | yes |
| `provider` | body | `string` | yes |
