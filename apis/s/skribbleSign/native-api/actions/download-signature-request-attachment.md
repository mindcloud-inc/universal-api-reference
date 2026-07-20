# Download Signature Request Attachment with Skribble Sign

Retrieves a signature request attachment from Skribble Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/signature-requests/:signatureRequestId/attachments/:attachmentId/content`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Download Signature Request Attachment](https://api-doc.skribble.com/#04a7353f-8a42-4645-a9f6-90723400fd0e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
| `attachmentId` | path | `string` | yes | The attachment ID. |
