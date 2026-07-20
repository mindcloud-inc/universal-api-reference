# Create Folder with Documo

Creates a new folder in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Create Folder](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | String \| Required \| Folder name |
| `sharedWithAccount` | body | `boolean` | no | Boolean \| Make the folder accessible by users across the account |
| `parentId` | body | `string` | no | Uuid \| Parent folder UUID |
| `userId` | body | `string` | no | Uuid \| UUID of the user who owns this folder |
