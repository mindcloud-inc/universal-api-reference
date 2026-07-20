# Restore Folder with GatherContent

Restores a trashed folder in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folder_uuid/restore`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Restore Folder](https://docs.gathercontent.com/reference/restorefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uuid` | path | `string` | yes | Folder UUID. |
