# Create Estimate with Housecall Pro

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Create Estimate](https://docs.housecallpro.com/docs/housecall-public-api/4004d373be14c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | no | — |
| `address_id` | body | `string` | no | — |
| `note` | body | `string` | no | — |
| `message` | body | `string` | no | — |
| `options[]` | body | `array<object>` | yes | — |
| `options[].name` | body | `string` | no | — |
| `options[].tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `options[].line_items[]` | body | `array<object>` | no | — |
| `schedule` | body | `object` | no | — |
| `schedule.start_time` | body | `date` | no | — |
| `schedule.end_time` | body | `date` | no | — |
| `schedule.arrival_window_in_minutes` | body | `number` | no | — |
| `schedule.notify_customer` | body | `boolean` | no | — |
| `assigned_employee_ids[]` | body | `array<string>` | no | Send multiple values as a array. |
| `lead_source` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `address.street` | body | `string` | no | — |
| `address.street_line_2` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `address.state` | body | `string` | no | — |
| `address.zip` | body | `string` | no | — |
| `tax` | body | `object` | no | — |
| `tax.taxable` | body | `boolean` | no | — |
| `tax.tax_rate` | body | `number` | no | — |
| `tax.tax_name` | body | `string` | no | — |
| `estimate_fields` | body | `object` | no | — |
| `estimate_fields.job_type_id` | body | `string` | no | — |
| `estimate_fields.business_unit_id` | body | `string` | no | — |
| `estimate_number` | body | `number` | no | Estimate number unique across all company estimates. If left blank, one will be generated automatically. |
