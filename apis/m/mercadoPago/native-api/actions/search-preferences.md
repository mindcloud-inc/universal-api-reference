# Search Preferences with Mercado Pago

Finds checkout preferences in Mercado Pago by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/checkout/preferences/search`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Search Preferences](https://www.mercadopago.com.ar/developers/en/reference/preferences/_checkout_preferences_search/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sponsor_id` | query | `number` | no |
| `external_reference` | query | `string` | no |
| `site_id` | query | `string` | no |
| `marketplace` | query | `string` | no |
