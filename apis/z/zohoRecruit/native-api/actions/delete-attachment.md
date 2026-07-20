# Delete Attachment with Zoho Recruit

Deletes an attachment from a Zoho Recruit record.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:moduleApiName/:recordId/Attachments/:attachmentId`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Delete Attachment](https://www.zoho.com/recruit/developer-guide/apiv2/delete-attachments.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `attachmentId` | path | `string` | yes | The unique ID of the attachment. |
