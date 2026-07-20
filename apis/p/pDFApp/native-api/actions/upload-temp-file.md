# Upload Temp File with PDF-app

Creates temporary file URLs in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadtempFile`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Upload Temp File](https://pdf-app.net/apidocumentation?type=uploadtempFile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrls[]` | body | `array<string>` | yes | Public file URLs to upload into PDF-app temporary storage. |
| `operationType` | body | `string` | no | Optional upload mode such as zip, upload, or download. |
| `fileType` | body | `string` | no | File type used when requesting a presigned upload URL. |
| `filePath` | body | `string` | no | Stored upload path used when requesting a presigned download URL. |
