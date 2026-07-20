# Search Merchant Orders with Mercado Pago

Finds merchant orders in Mercado Pago by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/merchant_orders/search`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Search Merchant Orders](https://www.mercadopago.com.ar/developers/en/reference/merchant_orders/_merchant_orders_search/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `preference_id` | query | `string` | no |
| `application_id` | query | `number` | no |
| `payer_id` | query | `number` | no |
| `sponsor_id` | query | `number` | no |
| `external_reference` | query | `string` | no |
| `site_id` | query | `string` | no |
| `marketplace` | query | `string` | no |
| `date_created_from` | query | `string` | no |
| `date_created_to` | query | `string` | no |
| `last_updated_from` | query | `string` | no |
| `last_updated_to` | query | `string` | no |
