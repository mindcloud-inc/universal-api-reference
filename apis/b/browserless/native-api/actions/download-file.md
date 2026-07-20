# Download File with Browserless

Downloads a file through Browserless browser automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/download`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Download File](https://docs.browserless.io/rest-apis/download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | JavaScript code that triggers a browser download. |
| `context` | body | `object` | no | Optional JSON object passed to the download code as context. |
