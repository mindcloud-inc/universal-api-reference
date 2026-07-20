# Get Nearest Bus Stops with OneMap SG

Retrieves nearest bus stops from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/nearbysvc/getNearestBusStops`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Get Nearest Bus Stops](https://www.onemap.gov.sg/apidocs/nearbytransport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | The latitude to search nearby bus stops around. |
| `longitude` | query | `number` | yes | The longitude to search nearby bus stops around. |
| `radius_in_meters` | query | `number` | no | The search radius in meters. |
