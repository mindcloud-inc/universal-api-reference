# Summarize content with 1minAI

Creates bullet-point content summaries in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Summarize content](https://docs.1min.ai/docs/api/ai-for-writing/content-summarizer/content-summarizer-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `numberOfBullet` | body | `number` | no |
| `numberOfWord` | body | `number` | no |
