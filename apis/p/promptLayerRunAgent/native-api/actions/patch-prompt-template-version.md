# Patch Prompt Template Version with PromptLayer Run Agent

Updates an existing prompt template version in PromptLayer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/prompt-templates/:identifier`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Patch Prompt Template Version](https://docs.promptlayer.com/reference/templates-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The prompt template name or ID to patch. |
| `version` | body | `number` | no | Optional base version number to patch from. |
| `label` | body | `string` | no | Optional release label identifying the base version to patch from. |
| `messages[]` | body | `array<object>` | no | Chat template message patch. Use an array for full replacement or an object keyed by string index for targeted patching. |
| `tools[]` | body | `array<object>` | no | Optional tools patch for chat templates. |
| `functions[]` | body | `array<object>` | no | Optional functions patch for chat templates. |
| `function_call` | body | `string` | no | Optional function_call patch for chat templates. |
| `tool_choice` | body | `string` | no | Optional tool_choice patch for chat templates. |
| `content[]` | body | `array<object>` | no | Completion template content patch for non-chat templates. |
| `model_parameters` | body | `object` | no | Optional model parameter patch. |
| `response_format` | body | `object` | no | Optional response_format patch. |
| `commit_message` | body | `string` | no | A message describing the new prompt template version. |
| `release_labels[]` | body | `array<string>` | no | Optional release labels to move or assign to the new version. |
