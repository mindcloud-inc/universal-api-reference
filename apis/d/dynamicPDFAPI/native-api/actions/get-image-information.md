# Get Image Information with DynamicPDF

Retrieves information about an image from DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/image-info`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Get Image Information](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-image-info)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `image/png` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Image` | body | `file` | yes | Image file sent as the raw request body. |
