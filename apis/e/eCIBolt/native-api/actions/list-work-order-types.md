# List Work Order Types with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/work_order_types`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Work Order Types](https://app.bolttech.net/api-docs/index.html#/Work_Order_Types/get_open_v1_work_order_types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed work_order_types, returned on the last page of the work_order_types. You should only send the refresh_token or the next_batch. |
