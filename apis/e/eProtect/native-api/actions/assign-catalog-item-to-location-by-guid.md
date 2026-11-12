# Assign Catalog Item to Location by GUID with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/inventory-assignment/catalog-guid-location-identifier/:cpcGuid/:targetLocationGuid`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Assign Catalog Item to Location by GUID](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1catalog-guid-location-identifier~1{cpcGuid}~1{targetLocationGuid}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cpcGuid` | path | `string` | yes | 3E catalog product GUID (unique record identifier). |
| `targetLocationGuid` | path | `string` | yes | Location GUID (unique record identifier) returned by List Locations. |
