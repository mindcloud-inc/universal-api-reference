# List Job Work Orders with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/jobs/:id/work_orders`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Job Work Orders](https://app.bolttech.net/api-docs/index.html#/Work_Orders/get_open_v1_jobs__id__work_orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the job. |
| `refresh_token` | query | `string` | no | Token used to get the changed work orders, returned on the last page of the work orders. You should only send the refresh_token or the next_batch. |
| `refresh` | query | `string` | no | Return only directly changed records when value is "self" |
