# Extract ChatGPT with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/chatgpt`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract ChatGPT](https://docs.cloro.dev/api-reference/endpoint/monitor-chatgpt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code for localized results. |
| `prompt` | body | `string` | yes | The prompt to send to ChatGPT. |
| `include` | body | `object` | no | Optional flags for additional response data. |
| `include.markdown` | body | `boolean` | no | Include markdown formatted response content. |
| `include.html` | body | `boolean` | no | Include HTML response content. |
| `include.rawResponse` | body | `boolean` | no | Include raw streaming response events. |
