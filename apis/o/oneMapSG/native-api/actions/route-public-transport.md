# Route (Public Transport) with OneMap SG

Retrieves a public transport route from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/routingsvc/route`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Route (Public Transport)](https://www.onemap.gov.sg/apidocs/routing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | The start location as latitude and longitude. |
| `end` | query | `string` | yes | The destination location as latitude and longitude. |
| `date` | query | `string` | yes | The travel date in MM-DD-YYYY format. |
| `time` | query | `string` | yes | The travel time in HH:mm:ss format. |
| `maxWalkDistance` | query | `number` | no | The maximum walking distance allowed for the route. |
| `numItineraries` | query | `number` | no | The number of itineraries to return. |
