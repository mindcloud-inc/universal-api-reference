# Search Flights with SearchApi

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://www.searchapi.io/api/v1`
- **Official documentation:** [Search Flights](https://www.searchapi.io/docs/google-flights-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `departure_id` | query | `string` | yes |
| `arrival_id` | query | `string` | yes |
| `outbound_date` | query | `string` | yes |
| `return_date` | query | `string` | yes |
