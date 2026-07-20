# Create Subscription with Reepay

Creates a new subscription in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Create Subscription](https://docs.frisbii.com/reference/createsubscriptionjson)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | no |
| `amount_incl_vat` | body | `boolean` | no |
| `cost_center` | body | `string` | no |
| `create_customer` | body | `object` | no |
| `customer` | body | `string` | no |
| `end_date` | body | `string` | no |
| `generate_handle` | body | `boolean` | no |
| `grace_duration` | body | `number` | no |
| `handle` | body | `string` | no |
| `metadata` | body | `object` | no |
| `no_setup_fee` | body | `boolean` | no |
| `no_trial` | body | `boolean` | no |
| `notice_period_unit_type` | body | `string` | no |
| `notice_periods` | body | `number` | no |
| `plan` | body | `string` | yes |
| `plan_version` | body | `number` | no |
| `po_number` | body | `string` | no |
| `quantity` | body | `number` | no |
| `show_terms` | body | `boolean` | no |
| `signup_method` | body | `string` | yes |
| `source` | body | `string` | no |
| `start_date` | body | `string` | no |
| `test` | body | `boolean` | no |
| `trial_period` | body | `string` | no |
