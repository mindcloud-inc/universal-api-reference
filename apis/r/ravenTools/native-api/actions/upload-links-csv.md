# Upload Links CSV with Raven Tools

Uploads links from a CSV file to Raven Tools.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [Upload Links CSV](https://api.raventools.com/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain whose links should receive the CSV import. |
| `monitor` | query | `string` | no | Set to 1 to enable link monitoring for uploaded links. |
| `file` | body | `file` | yes | Base64-encoded CSV content to upload to Raven Tools. |
