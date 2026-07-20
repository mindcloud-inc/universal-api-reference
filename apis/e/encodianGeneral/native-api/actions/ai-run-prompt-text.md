# AI Run Prompt Text with Encodian - General

Runs a custom AI text prompt in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AIRunPromptText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Run Prompt Text](https://support.encodian.com/hc/en-gb/articles/19106024843932)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The AI model to use for the prompt. |
| `prompt` | body | `string` | yes | Prompt text to process. |
