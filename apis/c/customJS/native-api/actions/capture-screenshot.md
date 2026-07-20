# Capture Screenshot with CustomJS

Captures a website screenshot in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/screenshot`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Capture Screenshot](https://www.customjs.space/integration/native-api/documentation/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.url` | body | `string` | yes | Website URL to capture. |
