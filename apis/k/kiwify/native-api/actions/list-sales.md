# List Sales with Kiwify

Retrieves sales from Kiwify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sales`
- **Base URL:** `https://public-api.kiwify.com`
- **Official documentation:** [List Sales](https://docs.kiwify.com.br/api-reference/sales/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `view_full_sale_details` | query | `boolean` | no |
| `payment_method` | query | `string` | no |
| `product_id` | query | `string` | no |
| `affiliate_id` | query | `string` | no |
| `page_size` | query | `string` | no |
| `page_number` | query | `string` | no |
| `start_date` | query | `string` | yes |
| `end_date` | query | `string` | yes |
| `updated_at_start_date` | query | `string` | no |
| `updated_at_end_date` | query | `string` | no |
