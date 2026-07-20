# List Airports with Airlabs

Retrieves airport database records from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/airports`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Airports](https://airlabs.co/docs/airports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Filter by country ISO 2 code. |
| `iata_code` | query | `string` | no | Filter by airport IATA code. |
| `icao_code` | query | `string` | no | Filter by airport ICAO code. |
