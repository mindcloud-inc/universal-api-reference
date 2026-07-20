# Generate blog article with 1minAI

Creates a blog article in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate blog article](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-blog-article)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `language` | body | `string` | no |
| `numberOfSection` | body | `number` | no |
| `numberOfWord` | body | `number` | no |
| `keywords` | body | `string` | no |
