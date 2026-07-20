# Shorten content with 1minAI

Creates shortened text content in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Shorten content](https://docs.1min.ai/docs/api/ai-for-writing/content-shortener/content-shortener-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `numberOfWord` | body | `number` | no |
