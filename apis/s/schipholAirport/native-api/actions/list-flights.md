# List Flights with Schiphol Airport

Retrieves flights from Schiphol Airport for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/flights`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [List Flights](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleDate` | query | `date` | no | Scheduled date to retrieve flights for, formatted YYYY-MM-DD. |
| `scheduleTime` | query | `string` | no | Scheduled time to retrieve flights from, formatted HH:mm. |
| `flightName` | query | `string` | no | Flight number as printed on the ticket, such as KL1234. |
| `flightDirection` | query | `string` | no | Flight direction: A for arrivals or D for departures. Accepted values: `0`, `1`. |
| `airline` | query | `string` | no | IATA or ICAO airline prefix, such as KL or KLM. |
| `airlineCode` | query | `number` | no | Schiphol numeric airline code. |
| `route` | query | `string` | no | IATA or ICAO route airport code; multiple values can be comma separated. |
| `includedelays` | query | `boolean` | no | Include earlier scheduled flights delayed into the requested date. |
| `page` | query | `number` | no | Result page number, starting at 0. |
| `sort` | query | `string` | no | Sort expression such as +scheduleTime or -scheduleDate,+scheduleTime. |
| `fromDateTime` | query | `string` | no | Start of a DateTime search range, formatted yyyy-MM-ddTHH:mm:ss. |
| `toDateTime` | query | `string` | no | End of a DateTime search range, formatted yyyy-MM-ddTHH:mm:ss. |
| `searchDateTimeField` | query | `string` | no | DateTime field to query when using fromDateTime and toDateTime. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `fromScheduleDate` | query | `date` | no | Start scheduled date for a scheduleDate range, formatted YYYY-MM-DD. |
| `toScheduleDate` | query | `date` | no | End scheduled date for a scheduleDate range, formatted YYYY-MM-DD. |
| `isOperationalFlight` | query | `boolean` | no | Filter by operational or non-operational flights. |
