# Get Payment with Ablefy

Retrieves a payment from Ablefy.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/payments/:id`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Get Payment](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Payment ID. |
| `amount` | query | `number` | no | — |
