# Execute Custom JavaScript with CustomJS

Executes custom JavaScript code in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/__js1-`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Execute Custom JavaScript](https://www.customjs.space/integration/native-api/documentation/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | JavaScript code to execute. |
| `input` | body | `string` | yes | Input payload made available to the JavaScript code. |
