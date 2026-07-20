# Generate comments with 1minAI

Creates social media comments in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate comments](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentType` | body | `list` | yes | Accepted values: `Facebook`, `LinkedIn`, `X`. |
| `prompt` | body | `string` | yes | — |
| `tone` | body | `string` | no | — |
| `language` | body | `string` | no | — |
