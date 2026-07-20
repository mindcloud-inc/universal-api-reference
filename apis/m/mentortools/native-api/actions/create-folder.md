# Create Folder with Mentortools

Creates a new folder in Mentortools.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediastorage/v1/folders`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Create Folder](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Folder name. |
| `parent_folder_id` | body | `number` | no | The parent folder ID. |
