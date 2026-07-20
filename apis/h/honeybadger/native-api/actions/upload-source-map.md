# Upload Source Map with Honeybadger

Uploads a source map to Honeybadger.

## Endpoint

- **Method:** `POST`
- **Path:** `/source_maps`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Upload Source Map](https://docs.honeybadger.io/api/reporting-source-maps/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minified_url` | body | `string` | yes | Absolute production URL for the minified JavaScript file. |
| `minified_file` | body | `file` | yes | The compiled minified JavaScript file. |
| `source_map` | body | `file` | yes | The source map file to upload. |
| `revision` | body | `string` | no | Deploy revision or code version for the uploaded source map. |
