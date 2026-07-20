# Add Signature Request Attachment with Skribble

Adds an attachment to a signature request in Skribble.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/signature-requests/:signatureRequestId/attachments`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Add Signature Request Attachment](https://api-doc.skribble.com/#8f8b71fd-3a23-4e88-b770-ea83090e41f2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The base64 encoded attachment content. |
| `content_type` | body | `string` | yes | The attachment MIME type. |
| `filename` | body | `string` | yes | The attachment filename. |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
