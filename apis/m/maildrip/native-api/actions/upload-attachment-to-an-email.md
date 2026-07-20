# Upload attachment To An Email with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/attachments/{email_id}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Upload attachment To An Email](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_id` | path | `string` | yes | ID of the email to upload the attachment to |
| `attachment` | body | `file` | yes | The attachment file to upload (Max 50kb) |
