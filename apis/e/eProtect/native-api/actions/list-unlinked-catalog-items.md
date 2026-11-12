# List Unlinked Catalog Items with 3E Protect

## Endpoint

- **Method:** `GET`
- **Path:** `/unlinked-catalog-item/:page/:source`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [List Unlinked Catalog Items](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1unlinked-catalog-item~1{page}~1{source}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
