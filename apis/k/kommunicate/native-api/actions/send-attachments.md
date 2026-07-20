# Send Attachments with Kommunicate

Creates an attachment message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Attachments](https://docs.kommunicate.io/docs/api-detail#send-attachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ofUserId` | body | `string` | yes | Admin user email to route into the required Of-User-Id header. |
| `type` | body | `number` | yes | Attachment type value from Kommunicate. |
| `contentType` | body | `number` | yes | Kommunicate content type code for the attachment message. |
| `message` | body | `string` | no | Optional attachment caption or description. |
| `groupId` | body | `string` | yes | Conversation identifier to send the attachment into. |
| `metadata` | body | `object` | no | Optional attachment metadata, for example skipBot. |
| `key` | body | `string` | yes | Kommunicate attachment key. |
| `fileMeta` | body | `object` | yes | File metadata object including blobKey and contentType. |
| `source` | body | `number` | yes | Kommunicate source value for the attachment message. |
