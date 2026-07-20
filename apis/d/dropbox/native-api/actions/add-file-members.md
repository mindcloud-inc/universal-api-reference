# Add File Members with Dropbox

Adds members to a shared file in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/add_file_member`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Add File Members](https://www.dropbox.com/developers/documentation/http/documentation#sharing-add_file_member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Path or ID of the file to share. |
| `memberEmails[]` | body | `array<string>` | yes | Email addresses to invite to the file. |
| `custom_message` | body | `string` | no | Optional message included with the invite. |
| `quiet` | body | `boolean` | no | When true, suppresses notification emails when possible. |
| `access_level` | body | `string` | no | Access level to grant to the invited members. |
| `add_message_as_comment` | body | `boolean` | no | Add the custom message as a comment on the file. |
