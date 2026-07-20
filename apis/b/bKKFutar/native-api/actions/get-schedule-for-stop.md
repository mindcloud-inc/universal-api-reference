# Get Schedule For Stop with BKK Futar

Retrieves the schedule for a selected BKK Futar stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedule-for-stop.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Get Schedule For Stop](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-schedule-for-stop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | query | `string` | yes | Stop ID to query, such as BKK_F01227. |
| `date` | query | `string` | no | Requested date in YYYYMMDD format. |
| `onlyDepartures` | query | `boolean` | no | Return departures only. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
