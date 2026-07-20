# Track Prompt with PromptLayer Run Agent

Tracks prompts in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/track-prompt`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Track Prompt](https://docs.promptlayer.com/reference/track-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt_name` | body | `string` | yes | Prompt template name to associate with the request. |
| `request_id` | body | `number` | yes | PromptLayer request ID to update. |
| `prompt_input_variables` | body | `object` | no | Input variables used for the prompt template. |
| `version` | body | `number` | no | Prompt template version number. Mutually exclusive with label. |
| `label` | body | `string` | no | Prompt template release label. Mutually exclusive with version. |
