# Extract Microsoft Copilot with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/copilot`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Microsoft Copilot](https://docs.cloro.dev/api-reference/endpoint/monitor-copilot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Country/region code for localized response. |
| `prompt` | body | `string` | yes | The prompt to send to Microsoft Copilot. |
| `include` | body | `object` | no | Optional flags for additional response formats. |
| `include.markdown` | body | `boolean` | no | Include markdown formatted response content. |
| `include.html` | body | `boolean` | no | Include HTML response content. |
