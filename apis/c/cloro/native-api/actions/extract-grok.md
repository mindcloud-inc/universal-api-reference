# Extract Grok with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/grok`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Grok](https://docs.cloro.dev/api-reference/endpoint/monitor-grok)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Country/region code for localized response. |
| `prompt` | body | `string` | yes | The prompt to send to Grok. |
| `include` | body | `object` | no | Optional flags for additional response formats. |
| `include.markdown` | body | `boolean` | no | Include markdown formatted response content. |
| `include.html` | body | `boolean` | no | Include HTML response content. |
