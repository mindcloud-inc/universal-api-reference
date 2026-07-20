# List Airlines with Airlabs

Retrieves airline database records from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/airlines`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Airlines](https://airlabs.co/docs/airlines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Filter by country ISO 2 code. |
| `iata_code` | query | `string` | no | Filter by airline IATA code. |
| `icao_code` | query | `string` | no | Filter by airline ICAO code. |
| `name` | query | `string` | no | Filter by airline name. |
