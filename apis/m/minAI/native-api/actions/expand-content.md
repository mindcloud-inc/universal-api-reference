# Expand content with 1minAI

Creates expanded text content in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Expand content](https://docs.1min.ai/docs/api/ai-for-writing/content-expander/content-expander-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `numberOfWord` | body | `number` | no |
