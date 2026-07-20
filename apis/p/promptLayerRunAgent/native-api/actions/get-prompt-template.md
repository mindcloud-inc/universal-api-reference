# Get Prompt Template with PromptLayer Run Agent

Retrieves a prompt template from PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/prompt-templates/:identifier`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Prompt Template](https://docs.promptlayer.com/reference/templates-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The prompt template name or ID. |
| `version` | body | `number` | no | Optional version number to retrieve. |
| `workspace_id` | body | `number` | no | Optional workspace override. |
| `label` | body | `string` | no | Optional release label to retrieve. |
| `provider` | body | `list` | no | Optional provider used for default llm_kwargs resolution. Accepted values: `0`, `1`. |
| `input_variables` | body | `object` | no | Optional input variables used to render the prompt template. |
| `metadata_filters` | body | `object` | no | Optional metadata filters used for A/B label selection. |
| `model` | body | `string` | no | Optional model name used to return default llm_kwargs. |
| `model_parameter_overrides` | body | `object` | no | Optional provider-specific model parameter overrides. |
