# Create Flight Alert Listener with Airlabs

Creates a flight alert listener in Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/listen`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [Create Flight Alert Listener](https://airlabs.co/docs/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_url` | query | `string` | yes | Server URL to receive incoming flight alert webhook updates. |
| `flight_number` | query | `string` | no | Listen for changes by flight number. |
| `airline_iata` | query | `string` | no | Listen for changes by airline IATA code. |
| `airline_icao` | query | `string` | no | Listen for changes by airline ICAO code. |
| `dep_iata` | query | `string` | no | Listen for changes by departure airport IATA code. |
| `dep_icao` | query | `string` | no | Listen for changes by departure airport ICAO code. |
| `dep_date` | query | `date` | no | Listen for changes by departure date. |
| `dep_time` | query | `string` | no | Listen for changes by departure time. |
| `arr_iata` | query | `string` | no | Listen for changes by arrival airport IATA code. |
| `arr_icao` | query | `string` | no | Listen for changes by arrival airport ICAO code. |
| `arr_date` | query | `date` | no | Listen for changes by arrival date. |
| `arr_time` | query | `string` | no | Listen for changes by arrival time. |
| `_fields` | query | `string` | no | Comma-separated fields to listen for, or leave empty to listen for all changes. |
