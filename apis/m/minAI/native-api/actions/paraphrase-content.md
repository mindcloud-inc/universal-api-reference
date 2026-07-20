# Paraphrase content with 1minAI

Creates paraphrased text content in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Paraphrase content](https://docs.1min.ai/docs/api/ai-for-writing/content-paraphraser/content-paraphraser-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `numberOfSection` | body | `number` | no |
| `numberOfWord` | body | `number` | no |
