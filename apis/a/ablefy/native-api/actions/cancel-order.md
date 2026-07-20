# Cancel Order with Ablefy

Updates an order in Ablefy by canceling it.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/orders/:token/cancel`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Cancel Order](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | Order token. |
