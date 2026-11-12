# Get Location by GUID with 3E Protect

## Endpoint

- **Method:** `GET`
- **Path:** `/location/guid/:locationGuid`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [Get Location by GUID](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location~1guid~1{locationGuid}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationGuid` | path | `string` | yes | Location GUID (unique record identifier) returned by List Locations. |
