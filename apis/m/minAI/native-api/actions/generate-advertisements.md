# Generate advertisements with 1minAI

Creates advertisement copy drafts in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate advertisements](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-advertisements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adPlatform` | body | `list` | yes | Accepted values: `Facebook`, `Google`. |
| `prompt` | body | `string` | yes | — |
| `tone` | body | `string` | no | — |
| `language` | body | `string` | no | — |
