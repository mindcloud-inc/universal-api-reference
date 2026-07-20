# Update Leave Request with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/leave_requests/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Leave Request](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Leave request ID. |
| `start_date` | body | `string` | yes | Leave request start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Leave request end date in YYYY-MM-DD format. |
| `type` | body | `number` | yes | Leave type ID. |
| `user` | body | `number` | yes | User ID requesting leave. |
