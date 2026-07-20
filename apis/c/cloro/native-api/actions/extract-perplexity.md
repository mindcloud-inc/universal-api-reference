# Extract Perplexity with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/perplexity`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Perplexity](https://docs.cloro.dev/api-reference/endpoint/monitor-perplexity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Country/region code for localized response. |
| `prompt` | body | `string` | yes | The prompt to send to Perplexity. |
| `include` | body | `object` | no | Optional flags for additional response formats. |
| `include.markdown` | body | `boolean` | no | Include markdown formatted response content. |
| `include.html` | body | `boolean` | no | Include HTML response content. |
