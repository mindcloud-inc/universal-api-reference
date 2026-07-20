# Upload Bulk Email List with Bouncify

Uploads a bulk email list to Bouncify.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk`
- **Base URL:** `https://api.bouncify.io/v1`
- **Official documentation:** [Upload Bulk Email List](https://bouncify.io/docs/api-docs/bulk-validation/upload-bulk-email-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_verify` | body | `string` | no | Set true to upload the list and immediately start verification. |
| `emails` | body | `object` | yes | Array of email objects to upload for bulk verification. Send multiple values as a array. |
| `title` | body | `string` | no | Friendly name for the bulk verification list. |
