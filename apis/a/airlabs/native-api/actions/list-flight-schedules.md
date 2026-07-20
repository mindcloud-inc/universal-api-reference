# List Flight Schedules with Airlabs

Retrieves upcoming flight schedules from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Flight Schedules](https://airlabs.co/docs/schedules)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_fields` | query | `string` | no | Comma-separated fields to return. |
| `airline_iata` | query | `string` | no | Query or filter by airline IATA code. |
| `arr_iata` | query | `string` | no | Query by arrival airport IATA code. |
| `dep_iata` | query | `string` | no | Query by departure airport IATA code. |
| `flight_iata` | query | `string` | no | Query by flight IATA code-number. |
