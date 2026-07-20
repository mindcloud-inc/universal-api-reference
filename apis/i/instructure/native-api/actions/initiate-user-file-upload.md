# Initiate User File Upload with Instructure

Initiates a user file upload in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/self/files`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Initiate User File Upload](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.create_file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | body | `string` | no | MIME type of the file. |
| `name` | body | `string` | yes | Name of the file to upload. |
| `parent_folder_id` | body | `string` | no | Folder ID to upload into. |
| `size` | body | `number` | yes | Size of the file in bytes. |
