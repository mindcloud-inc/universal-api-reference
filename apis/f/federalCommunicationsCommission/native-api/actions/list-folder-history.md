# List Folder History with Federal Communications Commission

Retrieves FCC OPIF folder change history.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/folder/history.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Folder History](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Number of folders in the list. |
| `endDate` | query | `string` | no | End date in YYYY-MM-DD format. |
| `entityId` | query | `string` | no | Unique entity ID. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `offset` | query | `string` | no | Starting row number. |
| `startDate` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `status` | query | `string` | no | Folder status filter. |
