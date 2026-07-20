# Calculate Flight Duration with SharpAPI

Retrieves flight duration details from SharpAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/airports/flight_duration/:departureCodeType/:departureCode/:departureDate/:departureTime/:arrivalCodeType/:arrivalCode/:arrivalDate/:arrivalTime`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Calculate Flight Duration](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departureCodeType` | path | `string` | yes | Departure airport code type, such as IATA. |
| `departureCode` | path | `string` | yes | Departure airport code. |
| `departureDate` | path | `string` | yes | Departure local date in YYYY-MM-DD format. |
| `departureTime` | path | `string` | yes | Departure local time in HH:MM format. |
| `arrivalCodeType` | path | `string` | yes | Arrival airport code type, such as IATA. |
| `arrivalCode` | path | `string` | yes | Arrival airport code. |
| `arrivalDate` | path | `string` | yes | Arrival local date in YYYY-MM-DD format. |
| `arrivalTime` | path | `string` | yes | Arrival local time in HH:MM format. |
