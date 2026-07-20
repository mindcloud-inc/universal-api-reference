# Get Folder by ID with Federal Communications Commission

Retrieves an FCC OPIF folder and its contents.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/folder/id/{folderId}.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Folder by ID](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Unique entity ID. |
| `folderId` | path | `string` | no | Unique ID of the folder. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
