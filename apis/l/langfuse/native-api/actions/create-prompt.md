# Create Prompt with Langfuse

Creates a new prompt version in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/prompts`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Prompt](https://api.reference.langfuse.com/#tag/Prompts/POST/api/public/v2/prompts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commitMessage` | body | `string` | no |
| `config` | body | `string` | no |
| `labels` | body | `string` | no |
| `name` | body | `string` | no |
| `prompt` | body | `string` | no |
| `tags` | body | `string` | no |
| `type` | body | `string` | no |
