# Search Subscriptions with Mercado Pago

Finds subscriptions in Mercado Pago by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/preapproval/search`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Search Subscriptions](https://www.mercadopago.com.ar/developers/en/reference/subscriptions/_preapproval_search/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | no |
| `payer_id` | query | `number` | no |
| `payer_email` | query | `string` | no |
| `preapproval_plan_id` | query | `string` | no |
