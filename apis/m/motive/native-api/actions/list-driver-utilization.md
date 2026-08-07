# List driver utilization with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/driver_utilization`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List driver utilization](https://developer-docs.gomotive.com/reference/fetch-the-utilization-of-the-driver-v2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_ids` | query | `list<number>` | no | Filter utilization by one or more driver IDs. Send multiple values as a array. |
| `start_date` | query | `date` | no | Fetch utilization from this date onward. |
| `end_date` | query | `date` | no | Fetch utilization through this date. |
