# Get Prompt with Langfuse

Retrieves a prompt from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/prompts/:promptName`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Get Prompt](https://api.reference.langfuse.com/#tag/Prompts/GET/api/public/v2/prompts/{promptName})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | query | `string` | no |
| `promptName` | path | `string` | no |
| `resolve` | query | `string` | no |
| `version` | query | `string` | no |
