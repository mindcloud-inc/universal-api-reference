# Rename Folder with GatherContent

Renames an existing folder in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folder_uuid/rename`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Rename Folder](https://docs.gathercontent.com/reference/renamefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uuid` | path | `string` | yes | Folder UUID. |
| `name` | body | `string` | yes | Folder name. |
