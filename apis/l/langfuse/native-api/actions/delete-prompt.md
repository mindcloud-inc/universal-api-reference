# Delete Prompt with Langfuse

Deletes prompt versions from Langfuse.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/prompts/:promptName`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Delete Prompt](https://api.reference.langfuse.com/#tag/Prompts/DELETE/api/public/v2/prompts/{promptName})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | query | `string` | no |
| `promptName` | path | `string` | no |
| `version` | query | `string` | no |
