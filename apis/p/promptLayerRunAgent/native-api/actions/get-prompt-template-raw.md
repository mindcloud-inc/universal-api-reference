# Get Prompt Template Raw with PromptLayer Run Agent

Retrieves a raw prompt template from PromptLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/prompt-templates/:identifier`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Prompt Template Raw](https://docs.promptlayer.com/reference/templates-get-raw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The prompt template name or ID. |
| `version` | query | `number` | no | Specific version number to retrieve. |
| `label` | query | `string` | no | Release label name to retrieve. |
| `resolve_snippets` | query | `boolean` | no | Whether to expand snippet references in the returned template. |
| `include_llm_kwargs` | query | `boolean` | no | Whether to include provider-specific llm_kwargs in the response. |
