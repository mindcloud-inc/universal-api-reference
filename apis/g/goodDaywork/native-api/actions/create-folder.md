# Create Folder with GoodDay.work

Creates a new folder in GoodDay.work.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/new-folder`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Create Folder](https://www.goodday.work/developers/api-v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdByUserId` | body | `string` | yes | ID of user on whose behalf folder is created. |
| `name` | body | `string` | yes | Folder name. |
| `parentProjectId` | body | `string` | no | Parent project ID for subfolder. |
