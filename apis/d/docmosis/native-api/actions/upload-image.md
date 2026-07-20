# Upload Image with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadImage`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Upload Image](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=47)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageFile` | body | `file` | yes | Image file stream to upload. |
| `imageName` | body | `string` | no | Override name and optional folder path for the uploaded image. |
| `imageDescription` | body | `string` | no | Short description for the uploaded image. |
| `normalizeImageName` | body | `boolean` | no | Normalize the uploaded image name using Unicode NFC. |
