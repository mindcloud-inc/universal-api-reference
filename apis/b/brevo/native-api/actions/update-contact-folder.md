# Update Contact Folder with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/contacts/folders/:folderId`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Contact Folder](https://developers.brevo.com/reference/updatefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `number` | yes | The contact folder identifier. |
| `name` | body | `string` | yes | The updated contact folder name. |
