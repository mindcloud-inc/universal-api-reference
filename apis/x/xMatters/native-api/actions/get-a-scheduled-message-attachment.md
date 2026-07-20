# Get a scheduled message attachment with xMatters

Retrieves a scheduled message attachment from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `scheduled-messages/{scheduledMessageId}/attachments/{attachmentId}`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get a scheduled message attachment](https://help.xmatters.com/xmapi/index.html#get-a-scheduled-message-attachment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attachmentId` | path | `string` | no |
| `scheduledMessageId` | path | `string` | no |
