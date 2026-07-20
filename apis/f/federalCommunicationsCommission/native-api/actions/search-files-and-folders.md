# Search Files and Folders with Federal Communications Commission

Finds FCC OPIF files and folders by search key.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/manager/search/key/{searchKey}.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Search Files and Folders](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Unique entity ID. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `searchKey` | path | `string` | no | Search key for files and folders. |
