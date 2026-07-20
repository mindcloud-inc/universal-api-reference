# Get Nearest MRT Stops with OneMap SG

Retrieves nearest MRT stops from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/nearbysvc/getNearestMrtStops`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Get Nearest MRT Stops](https://www.onemap.gov.sg/apidocs/nearbytransport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | The latitude to search nearby MRT stops around. |
| `longitude` | query | `number` | yes | The longitude to search nearby MRT stops around. |
| `radius_in_meters` | query | `number` | no | The search radius in meters. |
