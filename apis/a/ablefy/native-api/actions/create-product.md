# Create Product with Ablefy

Creates a new product in Ablefy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/products`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Create Product](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `forward.campaign_id` | body | `string` | no | — |
| `forward.coupon` | body | `string` | no | — |
| `forward.email` | body | `string` | no | — |
| `forward.first_name` | body | `string` | no | — |
| `forward.last_name` | body | `string` | no | — |
| `name` | body | `string` | yes | Product name. |
| `prices_attributes[].id` | body | `number` | no | — |
| `prices_attributes[].position` | body | `number` | no | — |
| `prices_attributes[].pricing_plan_id` | body | `number` | no | — |
| `success_email.body_de` | body | `string` | no | — |
| `success_email.body_en` | body | `string` | no | — |
| `success_email.subject_de` | body | `string` | no | — |
| `success_email.subject_en` | body | `string` | no | — |
| `team_members[].commission` | body | `number` | no | — |
| `team_members[].id` | body | `number` | no | — |
| `success_url` | body | `string` | no | — |
| `cancel_url` | body | `string` | no | — |
| `error_url` | body | `string` | no | — |
| `webhook_endpoint_ids[]` | body | `array<string>` | no | — |
| `webhook_url` | body | `string` | no | — |
| `page_header` | body | `string` | no | — |
| `page_footer` | body | `string` | no | — |
| `free` | body | `boolean` | no | — |
| `active` | body | `boolean` | no | — |
| `private` | body | `boolean` | no | — |
| `performance_period` | body | `boolean` | no | — |
| `performance_period_type` | body | `list<string>` | no | Accepted values: `custom_text`, `purchase_date`, `relative_date`. |
| `performance_period_text` | body | `string` | no | — |
| `form` | body | `list<string>` | no | Accepted values: `course`, `download`, `event`, `service`. |
| `webhook_endpoint_form` | body | `list<string>` | no | Accepted values: `all_webhook_endpoints`, `no_webhook_endpoints`, `selected_webhook_endpoints`. |
| `forward` | body | `object` | no | — |
| `team_members[]` | body | `array<object>` | no | — |
| `prices_attributes[]` | body | `array<object>` | no | — |
| `success_email` | body | `object` | no | — |
