# Remove Signature Request Attachment with Skribble Sign

Deletes a signature request attachment from Skribble Sign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/signature-requests/:signatureRequestId/attachments/:attachmentId`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Remove Signature Request Attachment](https://api-doc.skribble.com/#de1edd9b-bef3-4c59-a3c0-744421b1ae61)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
| `attachmentId` | path | `string` | yes | The attachment ID. |
