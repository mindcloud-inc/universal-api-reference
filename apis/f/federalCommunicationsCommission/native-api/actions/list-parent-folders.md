# List Parent Folders with Federal Communications Commission

Retrieves FCC OPIF parent folders.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/folder/parentFolders.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Parent Folders](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Unique entity ID. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `sourceService` | query | `string` | no | Source service code. |
