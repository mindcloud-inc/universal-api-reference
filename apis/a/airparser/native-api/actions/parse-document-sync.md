# Parse Document Sync with Airparser

Parses a document synchronously in Airparser.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inbox_id/upload-sync`
- **Base URL:** `https://api.airparser.com`
- **Official documentation:** [Parse Document Sync](https://help.airparser.com/public-api/public-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The Airparser inbox ID. |
| `file` | body | `file` | yes | The file to upload for parsing. |
| `meta` | body | `string` | no | Optional JSON string included in the parsed output as __meta__. |
