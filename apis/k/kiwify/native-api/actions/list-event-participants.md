# List Event Participants with Kiwify

Retrieves event participants from Kiwify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:product_id/participants`
- **Base URL:** `https://public-api.kiwify.com`
- **Official documentation:** [List Event Participants](https://docs.kiwify.com.br/api-reference/events/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | path | `string` | yes |
| `checked_in` | query | `boolean` | no |
| `page_size` | query | `string` | no |
| `page_number` | query | `string` | no |
| `created_at_start_date` | query | `string` | no |
| `created_at_end_date` | query | `string` | no |
| `updated_at_start_date` | query | `string` | no |
| `updated_at_end_date` | query | `string` | no |
| `external_id` | query | `string` | no |
| `batch_id` | query | `string` | no |
| `phone` | query | `string` | no |
| `cpf` | query | `string` | no |
| `order_id` | query | `string` | no |
