# Analyze HTML Article Bundle with TXT Werk

Analyzes an HTML article bundle in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Analyze HTML Article Bundle](https://services.txtwerk.de/ws/documentation/showRequest)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlFile` | body | `file` | yes | HTML article content file. |
| `language` | body | `string` | no | Optional input language. |
