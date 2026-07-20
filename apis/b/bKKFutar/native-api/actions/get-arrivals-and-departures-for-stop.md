# Get Arrivals And Departures For Stop with BKK Futar

Retrieves arrivals and departures for a BKK Futar stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/arrivals-and-departures-for-stop.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Get Arrivals And Departures For Stop](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-arrivals-and-departures-for-stop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | query | `string` | yes | Stop ID to query, such as BKK_F01227. |
| `minutesBefore` | query | `number` | no | Minutes before the query time to include. |
| `minutesAfter` | query | `number` | no | Minutes after the query time to include. |
| `includeRouteId` | query | `string` | no | Comma-separated route IDs used to filter results. |
| `time` | query | `number` | no | Epoch seconds timestamp used for the query. |
| `onlyDepartures` | query | `boolean` | no | Return departures only. |
| `limit` | query | `number` | no | Maximum number of returned stop times. |
| `lat` | query | `number` | no | Latitude information of the location. |
| `lon` | query | `number` | no | Longitude information of the location. |
| `radius` | query | `number` | no | Radius around latitude and longitude. |
| `query` | query | `string` | no | Query expression used to filter results. |
| `minResult` | query | `number` | no | Minimum number of elements returned. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
