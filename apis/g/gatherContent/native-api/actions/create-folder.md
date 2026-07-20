# Create Folder with GatherContent

Creates a new folder in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folder_uuid/folders`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Create Folder](https://docs.gathercontent.com/reference/createfolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uuid` | path | `string` | yes | Parent folder UUID. |
| `name` | body | `string` | no | Folder name. |
