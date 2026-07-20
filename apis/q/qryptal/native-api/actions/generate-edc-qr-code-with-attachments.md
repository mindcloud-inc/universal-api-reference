# Generate EDC QR Code With Attachments with Qryptal

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`
- **Official documentation:** [Generate EDC QR Code With Attachments](https://dash2.qryptal.com/docs/api2-api/#api-call-generate-qr-edc)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `string` | yes | JSON string containing the Qryptal payload with data, format, and scheme. |
| `img1` | body | `file` | no | Optional image attachment for the multipart field named img1. |
| `file1` | body | `file` | no | Optional document attachment for the multipart field named file1. |
