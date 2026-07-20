# Get Folder by Path with Federal Communications Commission

Retrieves an FCC OPIF folder by path.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/folder/path.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Folder by Path](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Unique entity ID. |
| `folderPath` | query | `string` | no | Complete folder path. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `sourceService` | query | `string` | no | Source service code. |
