# Get Refund with Mercado Pago

Retrieves a refund from Mercado Pago.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/{id}/refunds/{refund_id}`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Get Refund](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_id_refunds_refund_id/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `refund_id` | path | `number` | yes |
