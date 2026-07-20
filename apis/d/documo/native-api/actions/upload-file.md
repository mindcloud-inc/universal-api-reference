# Upload File with Documo

Uploads a new file to Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Upload File](https://docs.documo.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `file` | yes | File \| Required |
| `isPublic` | body | `boolean` | no | Boolean \| Makes file accessible by direct link stored in publicHref |
| `sharedWithAccount` | body | `boolean` | no | Boolean \| Make this file accessible by users across the account |
| `folderId` | body | `string` | no | Uuid \| UUID of the folder where the file will reside |
| `userId` | body | `string` | no | Uuid \| UUID of the user who owns this folder |
