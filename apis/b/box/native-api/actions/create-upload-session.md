# Create Upload Session with Box

## Endpoint

- **Method:** `POST`
- **URL:** `https://upload.box.com/api/2.0/files/upload_sessions`
- **Official documentation:** [Create Upload Session](https://developer.box.com/reference/post-files-upload-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | body | `string` | yes | Parent Box folder ID. Use `0` for the root folder. |
| `file_size` | body | `number` | yes | Total file size in bytes, not the length of its base64 representation. |
| `file_name` | body | `string` | yes | Name of the file to upload. |
