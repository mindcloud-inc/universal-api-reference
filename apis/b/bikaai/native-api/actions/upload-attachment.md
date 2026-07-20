# Upload Attachment with Bika.ai

Uploads an attachment to Bika.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:spaceId/attachments`
- **Base URL:** `https://bika.ai/api/openapi/bika/v1`
- **Official documentation:** [Upload Attachment](https://bika.ai/help/guide/developer/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Bika.ai workspace/space ID. |
| `file` | body | `file` | yes | File to upload as multipart form data. |
