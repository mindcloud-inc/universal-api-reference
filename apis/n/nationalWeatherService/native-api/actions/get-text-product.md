# Get Text Product with National Weather Service

Retrieves a text product from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:productId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Text Product](https://api.weather.gov/openapi.json#/paths/~1products~1{productId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | no | NWS text product identifier. |
