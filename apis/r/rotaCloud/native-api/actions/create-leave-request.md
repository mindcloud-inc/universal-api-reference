# Create Leave Request with RotaCloud

Requests leave in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/leave_requests`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Leave Request](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | body | `string` | yes | Leave request end date in ISO format. |
| `start_date` | body | `string` | yes | Leave request start date in ISO format. |
| `type` | body | `number` | yes | Leave type ID. |
| `user` | body | `number` | yes | User ID requesting leave. |
