# Move Folder with GatherContent

Moves an existing folder in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folder_uuid/move`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Move Folder](https://docs.gathercontent.com/reference/movefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uuid` | path | `string` | yes | Folder UUID. |
| `parent_uuid` | body | `string` | yes | Destination parent folder UUID. |
