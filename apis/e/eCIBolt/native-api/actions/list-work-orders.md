# List Work Orders with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/work_orders`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Work Orders](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_work_orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed work orders, returned on the last page of the work orders. You should only send the refresh_token or the next_batch. |
