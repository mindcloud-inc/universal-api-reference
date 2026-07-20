# List Real-Time Flights with Airlabs

Retrieves real-time flight data from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/flights`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Real-Time Flights](https://airlabs.co/docs/flights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_fields` | query | `string` | no | Comma-separated fields to return. |
| `airline_iata` | query | `string` | no | Filter by airline IATA code. |
| `arr_iata` | query | `string` | no | Filter by arrival airport IATA code. |
| `bbox` | query | `string` | no | Bounding box as south-west latitude, south-west longitude, north-east latitude, north-east longitude. |
| `dep_iata` | query | `string` | no | Filter by departure airport IATA code. |
| `flight_iata` | query | `string` | no | Filter by flight IATA code-number, such as AA6. |
