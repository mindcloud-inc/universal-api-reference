# Upload Media with Placid

Uploads media to Placid and returns reusable file URLs.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/media`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Upload Media](https://placid.app/docs/2.0/rest/media)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | Default multipart file field. Placid also supports additional custom file field names. |
