# Update Campaign with ActiveTrail

Updates an existing campaign in ActiveTrail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:id`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Update Campaign](https://webapi.mymarketing.co.il/api/docs/and/Api/PUT-api-campaigns-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a_b_settings` | body | `object` | no | A/B settings. |
| `a_b_settings.ab_percent_split_groups` | body | `number` | no | — |
| `a_b_settings.google_analytics_name` | body | `string` | no | — |
| `a_b_settings.scheduling` | body | `object` | no | — |
| `a_b_settings.scheduling.is_sent` | body | `boolean` | no | — |
| `a_b_settings.scheduling.scheduled_date_utc` | body | `date` | no | — |
| `a_b_settings.subject` | body | `string` | no | — |
| `a_b_settings.user_profile_id` | body | `number` | no | — |
| `carts` | body | `object` | no | E-commerce data list. |
| `carts.ecommerce_data[]` | body | `array<object>` | no | — |
| `design` | body | `object` | yes | Campaign design. |
| `design.content` | body | `string` | no | — |
| `design.header_footer_language_type` | body | `string` | no | — |
| `design.is_add_print_email` | body | `boolean` | no | — |
| `design.is_auto_css_inliner` | body | `boolean` | no | — |
| `design.is_remove_system_links` | body | `boolean` | no | — |
| `design.language_type` | body | `string` | no | — |
| `details` | body | `object` | yes | Campaign details. |
| `details.content_category_id` | body | `number` | no | — |
| `details.google_analytics_name` | body | `string` | no | — |
| `details.name` | body | `string` | no | — |
| `details.predictive_delivery` | body | `boolean` | no | — |
| `details.preheader` | body | `string` | no | — |
| `details.subject` | body | `string` | no | — |
| `details.user_profile_id` | body | `number` | no | — |
| `id` | path | `number` | yes | Campaign id. |
| `pairs[]` | body | `array<object>` | no | Replacement key-value pairs. |
| `pairs[].key` | body | `string` | no | — |
| `pairs[].value` | body | `string` | no | — |
| `send_test` | body | `string` | no | Email addresses to send a test email to, separated by commas. |
| `template` | body | `object` | no | Campaign template. |
| `template.id` | body | `number` | no | — |
