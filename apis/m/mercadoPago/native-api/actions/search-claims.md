# Search Claims with Mercado Pago

Finds claims in Mercado Pago by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/post-purchase/v1/claims/search`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Search Claims](https://www.mercadopago.com.ar/developers/en/reference/claims/search-claims/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `number` | no |
| `type` | query | `string` | no |
| `stage` | query | `string` | no |
| `status` | query | `string` | no |
| `resource` | query | `string` | no |
| `resource_id` | query | `number` | no |
