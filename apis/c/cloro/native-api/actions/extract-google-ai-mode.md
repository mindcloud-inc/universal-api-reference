# Extract Google AI Mode with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/aimode`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Google AI Mode](https://docs.cloro.dev/api-reference/endpoint/monitor-aimode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Country/region code for localized response. |
| `device` | body | `string` | no | Device type for AI Mode results. |
| `location` | body | `string` | no | Google canonical location name for city-level targeting. |
| `prompt` | body | `string` | yes | The prompt to send to Google AI Mode. |
| `uule` | body | `string` | no | Pre-encoded Google UULE string for precise geo-targeting. |
| `include` | body | `object` | no | Optional flags for additional response formats. |
| `include.markdown` | body | `boolean` | no | Include markdown formatted response content. |
| `include.html` | body | `boolean` | no | Include HTML response content. |
