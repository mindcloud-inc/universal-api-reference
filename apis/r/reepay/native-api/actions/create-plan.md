# Create Plan with Reepay

Creates a new plan in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/plan`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Create Plan](https://docs.frisbii.com/reference/createplanjson)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `amount_incl_vat` | body | `boolean` | no |
| `currency` | body | `string` | no |
| `description` | body | `string` | no |
| `dunning_plan` | body | `string` | no |
| `entitlements[]` | body | `array<string>` | no |
| `handle` | body | `string` | yes |
| `interval_length` | body | `number` | no |
| `metadata` | body | `object` | no |
| `name` | body | `string` | yes |
| `prepaid` | body | `boolean` | no |
| `quantity` | body | `number` | no |
| `schedule_fixed_day` | body | `number` | no |
| `schedule_fixed_hour` | body | `number` | no |
| `schedule_type` | body | `string` | yes |
| `setup_fee` | body | `number` | no |
| `tax_policy` | body | `string` | no |
| `trial_interval_length` | body | `number` | no |
| `trial_interval_unit` | body | `string` | no |
| `vat` | body | `number` | no |
