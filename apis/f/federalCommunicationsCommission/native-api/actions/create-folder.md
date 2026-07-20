# Create Folder with Federal Communications Commission

Creates a new FCC OPIF folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/manager/folder/create.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Create Folder](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessToken` | query | `string` | no | Entity access token required by FCC for folder creation, sent in the accessToken header by the documented endpoint. |
| `entityId` | body | `string` | no | Unique entity ID. |
| `folderName` | body | `string` | no | Name of the new folder. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `parentFolderId` | body | `string` | no | Unique ID of the parent folder. |
| `serviceCode` | body | `string` | no | Entity service code. |
