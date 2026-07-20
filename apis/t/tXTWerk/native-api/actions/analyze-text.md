# Analyze Text with TXT Werk

Analyzes text content in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Analyze Text](https://services.txtwerk.de/ws/documentation/showRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to analyze. |
| `services` | body | `string` | yes | Comma-separated analysis services to run. |
| `language` | body | `string` | no | Optional input language; omit to let TXT Werk detect it automatically. |
