# Update Folder with Wrike

Updates an existing folder in Wrike.

## Endpoint

- **Method:** `PUT`
- **Path:** `/folders/:folderId`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Update Folder](https://developers.wrike.com/api/v4/folders-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Wrike folder ID. |
| `title` | query | `string` | no | Title |
| `description` | query | `string` | no | Folder description |
| `addParents` | query | `string` | no | Folder IDs to add as parents, as a JSON string array |
| `removeParents` | query | `string` | no | Folder IDs to remove as parents, as a JSON string array |
| `addShareds` | query | `string` | no | User or invitation IDs to share with, as a JSON string array |
| `removeShareds` | query | `string` | no | User or invitation IDs to unshare, as a JSON string array |
| `metadata` | query | `string` | no | Metadata entries to update, as a JSON string array |
| `restore` | query | `boolean` | no | Restore folder from recycled bin |
| `customFields` | query | `string` | no | Custom field values to update, as a JSON string array |
| `customColumns` | query | `string` | no | Custom field IDs as a JSON string array |
| `clearCustomColumns` | query | `boolean` | no | Remove all custom fields associated with the folder |
| `project` | query | `string` | no | Project settings as a JSON object string |
| `addAccessRoles` | query | `string` | no | User ID for access role assignment |
| `removeAccessRoles` | query | `string` | no | User IDs whose access roles should be removed, as a JSON string array |
| `withInvitations` | query | `boolean` | no | Include invitations in owner and shared lists |
| `convertToCustomItemType` | query | `string` | no | Custom item type ID |
| `plainTextCustomFields` | query | `boolean` | no | Strip HTML tags from custom fields |
| `fields` | query | `string` | no | Response field names as a JSON string array |
