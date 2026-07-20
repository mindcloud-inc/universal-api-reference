# Search Payments with Mercado Pago

Finds payments in Mercado Pago by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/search`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Search Payments](https://www.mercadopago.com.ar/developers/en/reference/payments/_payments_search/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sort` | query | `string` | yes |
| `criteria` | query | `string` | yes |
| `external_reference` | query | `string` | yes |
| `range` | query | `string` | yes |
| `begin_date` | query | `string` | no |
| `end_date` | query | `string` | no |
| `store_id` | query | `number` | no |
| `pos_id` | query | `number` | no |
| `collector.id` | query | `number` | no |
| `payer.id` | query | `number` | no |
| `installments` | query | `number` | no |
| `payment_method_id` | query | `string` | no |
| `payment_type_id` | query | `string` | no |
| `operation_type` | query | `string` | no |
| `processing_mode` | query | `string` | no |
| `status` | query | `string` | no |
| `status_detail` | query | `string` | no |
