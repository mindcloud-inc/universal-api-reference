# Research keywords with 1minAI

Finds keyword ideas and metrics in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Research keywords](https://docs.1min.ai/docs/api/ai-for-writing/keyword-research/keyword-research-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `researchType` | body | `list` | yes | Accepted values: `Generate keywords`, `Keyword + statistics`, `Statistics`. |
| `prompt` | body | `string` | no | — |
| `numberOfWord` | body | `number` | no | — |
| `keywordList` | body | `string` | no | — |
