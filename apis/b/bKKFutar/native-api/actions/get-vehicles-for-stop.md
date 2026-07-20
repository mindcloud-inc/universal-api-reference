# Get Vehicles For Stop with BKK Futar

Retrieves vehicles on routes containing a selected BKK Futar stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/vehicles-for-stop.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Get Vehicles For Stop](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-vehicles-for-stop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | query | `string` | yes | Stop ID to query, such as BKK_F01227. |
| `ifModifiedSince` | query | `number` | no | Return data modified since this UNIX timestamp. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
