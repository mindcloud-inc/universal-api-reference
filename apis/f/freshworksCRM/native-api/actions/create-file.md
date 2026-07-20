# Create File with Freshworks CRM

Uploads a file to Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/documents`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create File](https://developers.freshworks.com/crm/api/#create_file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Binary file content or base64 payload |
| `file_name` | body | `string` | no | Optional file name used when uploading |
| `is_shared` | body | `boolean` | no | Share the uploaded file |
| `targetable_id` | body | `number` | yes | ID of the contact, sales account, deal, or product |
| `targetable_type` | body | `string` | yes | Entity type: Contact, SalesAccount, Deal, or Product |
