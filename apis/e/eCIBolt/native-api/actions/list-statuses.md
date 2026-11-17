# List Statuses with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/work_order_statuses`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Statuses](https://app.bolttech.net/api-docs/index.html#/Work_Order_Statuses/get_open_v1_work_order_statuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed statuses, returned on the last page of the statuses. You should only send the refresh_token or the next_batch. |
