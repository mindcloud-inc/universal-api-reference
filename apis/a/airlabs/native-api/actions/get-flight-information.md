# Get Flight Information with Airlabs

Retrieves current flight information from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/flight`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [Get Flight Information](https://airlabs.co/docs/flight)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flight_iata` | query | `string` | yes | Search by flight IATA code-number, such as AA6. Use this unless you have the ICAO code. |
| `flight_icao` | query | `string` | no | Alternative search by flight ICAO code-number. |
