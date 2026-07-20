# Create Folder in Room with Mural

Creates a new folder in a Mural room.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/folders`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Create Folder in Room](https://developers.mural.co/public/reference/createroomfolder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `roomId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `parentId` | body | `string` | no |
