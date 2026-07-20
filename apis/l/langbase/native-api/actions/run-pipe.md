# Run Pipe with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/pipes/run`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Run Pipe](https://langbase.com/docs/api-reference/pipe/run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Pipe name to run when using a user or org API key. |
| `messages[]` | body | `array<object>` | yes | Array of chat messages to send to the pipe. |
| `llmApiKey` | body | `string` | no | Optional provider LLM API key for the `LB-LLM-Key` request header. |
