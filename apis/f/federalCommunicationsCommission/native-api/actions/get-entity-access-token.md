# Get Entity Access Token with Federal Communications Commission

Retrieves an FCC entity access token.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/manager/get/entityAccessToken.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Entity Access Token](https://publicfiles.fcc.gov/json/opif-file-manager.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | body | `string` | no | Unique entity ID. |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, xml. |
| `serviceCode` | body | `string` | no | Entity service code. |
