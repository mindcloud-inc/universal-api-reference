# Get Catalog Item by GUID with 3E Protect

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog-item/guid/:productGuid`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Get Catalog Item by GUID](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1guid~1{productGuid}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productGuid` | path | `string` | yes | Use productUid from a Search Catalog Items result to retrieve that product's full details. |
