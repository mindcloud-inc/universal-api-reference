# Delete Folder with Cloudinary

Deletes a folder from your Cloudinary account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/folders/:folder`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Delete Folder](https://cloudinary.com/documentation/admin_api#delete_folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | path | `string` | yes | The full path of the empty folder to delete. |
| `skip_backup` | query | `boolean` | no | When true, also deletes the folder from backup storage. |
