# Add Shared Folder Members with Dropbox

Adds members to a shared folder in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/add_folder_member`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Add Shared Folder Members](https://www.dropbox.com/developers/documentation/http/documentation#sharing-add_folder_member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared_folder_id` | body | `string` | yes | ID of the shared folder to update. |
| `memberEmails[]` | body | `array<string>` | yes | Email addresses to invite to the shared folder. |
| `accessLevel` | body | `string` | no | Access level to grant to each invited member. |
| `quiet` | body | `boolean` | no | When true, suppresses notification emails when possible. |
| `custom_message` | body | `string` | no | Optional message included with the invite. |
