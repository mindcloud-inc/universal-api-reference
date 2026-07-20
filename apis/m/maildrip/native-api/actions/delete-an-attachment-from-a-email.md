# Delete an attachment from a email with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/attachments/`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete an attachment from a email](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | ID of the Email to delete attachment from |
| `attachmentId` | query | `string` | yes | ID of the attachment to delete |
