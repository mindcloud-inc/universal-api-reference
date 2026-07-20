# Upload Document Base64 with SigningHub

Uploads a base64 document to SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/base64`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Upload Document Base64](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UploadBase64)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the package to which the document is being added. |
| `document` | body | `string` | yes | Base64-encoded document content. |
