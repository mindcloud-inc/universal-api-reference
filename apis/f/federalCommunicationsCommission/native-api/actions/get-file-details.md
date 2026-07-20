# Get File Details with Federal Communications Commission

Retrieves FCC OPIF file details by file ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/file/id/{fileId}.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get File Details](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Unique entity ID. |
| `fileId` | path | `string` | no | Unique ID of the file. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
