# Enhance Prompt with Tinq.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/enhance-prompt`
- **Base URL:** `https://tinq.ai`
- **Official documentation:** [Enhance Prompt](https://docs.tinq.ai/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model identifier to enhance against. |
| `prompt` | body | `string` | yes | Prompt text to enhance. |
