# Get Media by File Name with Wati

Retrieves a media file from Wati by file name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/getMedia`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Get Media by File Name](https://docs.wati.io/reference/get_api-v1-getmedia)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | Media file name returned by Wati messages. |
