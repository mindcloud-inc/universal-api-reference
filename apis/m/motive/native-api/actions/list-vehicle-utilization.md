# List vehicle utilization with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/vehicle_utilization`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List vehicle utilization](https://developer-docs.gomotive.com/reference/fetch-the-utilization-of-the-driver-v2-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vehicle_ids` | query | `list<number>` | no | Filter utilization by one or more vehicle IDs. Send multiple values as a array. |
| `start_date` | query | `date` | no | Fetch utilization from this date onward. |
| `end_date` | query | `date` | no | Fetch utilization through this date. |
