# Update Prompt Version with Langfuse

Updates labels for a Langfuse prompt version.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/prompts/:name/versions/:version`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Update Prompt Version](https://api.reference.langfuse.com/#tag/PromptVersion/PATCH/api/public/v2/prompts/{name}/versions/{version})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | path | `string` | no |
| `newLabels` | body | `string` | no |
| `version` | path | `string` | no |
