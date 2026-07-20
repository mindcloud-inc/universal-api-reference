# Generate code with 1minAI

Creates code from a prompt in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate code](https://docs.1min.ai/docs/api/ai-for-code/code-generator/code-generator-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `webSearch` | body | `boolean` | no |
| `numOfSite` | body | `number` | no |
| `maxWord` | body | `number` | no |
