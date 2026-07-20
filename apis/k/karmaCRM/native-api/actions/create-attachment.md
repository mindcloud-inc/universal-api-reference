# Create Attachment with Karma CRM

Creates an attachment in Karma CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/attachments`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Create Attachment](https://docs.karmacrm.com/#create-an-attachment)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment[file]` | body | `string` | yes | File to attach. |
| `attachment[record_id]` | body | `number` | yes | ID of the record associated with the attachment. |
| `attachment[record_type]` | body | `string` | yes | Type of record associated with the attachment, for example Contact. |
