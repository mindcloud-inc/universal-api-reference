# List Cities with Airlabs

Retrieves city database records from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/cities`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Cities](https://airlabs.co/docs/cities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city_code` | query | `string` | no | Filter by IATA city code. |
| `country_code` | query | `string` | no | Filter by country ISO 2 code. |
