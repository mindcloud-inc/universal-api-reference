# Create Refund with Mercado Pago

Creates a refund in Mercado Pago.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payments/{id}/refunds`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Create Refund](https://www.mercadopago.com.ar/developers/en/reference/chargebacks/_payments_id_refunds/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `amount` | body | `number` | no |
