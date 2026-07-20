# Generate social media posts with 1minAI

Creates social media posts in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate social media posts](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-social-media-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postType` | body | `list` | yes | Accepted values: `Facebook`, `Instagram`, `LinkedIn`, `TikTok`, `X`. |
| `prompt` | body | `string` | yes | — |
| `tone` | body | `string` | no | — |
| `language` | body | `string` | no | — |
