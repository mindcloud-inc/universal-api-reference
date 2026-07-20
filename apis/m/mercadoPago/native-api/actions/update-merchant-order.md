# Update Merchant Order with Mercado Pago

Updates an existing merchant order in Mercado Pago.

## Endpoint

- **Method:** `PUT`
- **Path:** `/merchant_orders/{id}`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Update Merchant Order](https://www.mercadopago.com.ar/developers/en/reference/merchant_orders/_merchant_orders_id/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `external_reference` | body | `string` | no | — |
| `preference_id` | body | `string` | no | — |
| `marketplace` | body | `string` | no | — |
| `notification_url` | body | `string` | no | Use an HTTPS callback URL. |
