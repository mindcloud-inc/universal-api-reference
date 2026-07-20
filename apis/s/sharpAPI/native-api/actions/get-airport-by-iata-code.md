# Get Airport By Iata Code with SharpAPI

Retrieves an airport by IATA code from SharpAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/airports/iata/:iata`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Get Airport By Iata Code](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iata` | path | `string` | yes | IATA airport code. |
