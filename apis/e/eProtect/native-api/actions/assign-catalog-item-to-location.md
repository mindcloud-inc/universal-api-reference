# Assign Catalog Item to Location with 3E Protect

## Endpoint

- **Method:** `PUT`
- **Path:** `/inventory-assignment/:source/:identifier/:targetLocationGuid`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Assign Catalog Item to Location](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1{source}~1{identifier}~1{targetLocationGuid}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | path | `string` | yes | Your product identifier value for the selected source. |
| `targetLocationGuid` | path | `string` | yes | Location GUID (unique record identifier) returned by List Locations. |
