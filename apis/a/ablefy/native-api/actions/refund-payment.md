# Refund Payment with Ablefy

Updates a payment in Ablefy by refunding it.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/payments/:id/refund`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Refund Payment](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Payment ID. |
| `amount` | body | `number` | no | — |
