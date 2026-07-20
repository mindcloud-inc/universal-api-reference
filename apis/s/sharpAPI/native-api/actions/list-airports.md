# List Airports with SharpAPI

Retrieves airports from SharpAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/airports`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [List Airports](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `per_page` | query | `number` | no | Number of airports to return per page. |
