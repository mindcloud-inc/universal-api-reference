# Create Folder with Wrike

Creates a new folder in a Wrike folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folderId/folders`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Create Folder](https://developers.wrike.com/api/v4/folders-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Wrike parent folder ID where the folder will be created. |
| `title` | query | `string` | yes | Title, cannot be empty |
| `description` | query | `string` | no | Folder description |
| `shareds` | query | `string` | no | User or invitation IDs to share with, as a JSON string array |
| `metadata` | query | `string` | no | Metadata entries as a JSON string array |
| `customFields` | query | `string` | no | Custom field values as a JSON string array |
| `customColumns` | query | `string` | no | Custom field IDs as a JSON string array |
| `project` | query | `string` | no | Project settings as a JSON object string |
| `userAccessRoles` | query | `string` | no | User ID for access role assignment |
| `withInvitations` | query | `boolean` | no | Include invitations in owner and shared lists |
| `customItemTypeId` | query | `string` | no | Custom item type ID to create a project from |
| `plainTextCustomFields` | query | `boolean` | no | Strip HTML tags from custom fields |
| `fields` | query | `string` | no | Response field names as a JSON string array |
