# Upload File with Mentortools

Uploads a file to Mentortools.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediastorage/v1/files/upload`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Upload File](https://app.mentortools.com/public_api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload. |
| `parent_folder_id` | body | `number` | no | The parent folder ID. |
