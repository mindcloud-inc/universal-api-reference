# Upload Document with SigningHub

Uploads a document to SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Upload Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UploadStream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the package to which the document is being added. |
| `file (binary Stream)` | body | `string` | yes | Raw binary document content to upload. |
