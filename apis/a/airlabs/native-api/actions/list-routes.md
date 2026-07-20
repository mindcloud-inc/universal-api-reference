# List Routes with Airlabs

Retrieves airline route data from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/routes`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Routes](https://airlabs.co/docs/routes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airline_iata` | query | `string` | no | Filter by airline IATA code. |
| `arr_iata` | query | `string` | no | Filter by arrival airport IATA code. |
| `dep_iata` | query | `string` | no | Filter by departure airport IATA code. |
| `flight_iata` | query | `string` | no | Filter by flight IATA code-number. |
