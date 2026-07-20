# Generate emails with 1minAI

Creates email message drafts in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate emails](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailType` | body | `list` | yes | Accepted values: `Email`, `Reply`. |
| `prompt` | body | `string` | yes | — |
| `tone` | body | `string` | no | — |
| `language` | body | `string` | no | — |
