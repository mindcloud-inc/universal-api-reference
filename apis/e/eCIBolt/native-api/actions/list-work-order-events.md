# List Work Order Events with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/work_orders/events`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Work Order Events](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_token` | query | `string` | yes | Token used to get the next list of events. |
