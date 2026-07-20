# Get Uploaded File Info with Tolq

Retrieves uploaded file details from Tolq.

## Endpoint

- **Method:** `GET`
- **Path:** `/translations/requests/files/:uid`
- **Base URL:** `https://api.tolq.com/v1`
- **Official documentation:** [Get Uploaded File Info](https://docs.tolq.com/reference/uploaded-file-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | Uploaded file UID returned by Initiate File Upload. |
