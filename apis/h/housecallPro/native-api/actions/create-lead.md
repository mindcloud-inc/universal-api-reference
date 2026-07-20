# Create Lead with Housecall Pro

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Create Lead](https://docs.housecallpro.com/docs/housecall-public-api/8961eaf9f1c28-create-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | no | Either this or Customer is required. |
| `customer` | body | `object` | no | Either this or Customer ID is required. |
| `address_id` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `assigned_employee_id` | body | `string` | no | — |
| `lead_source` | body | `string` | no | — |
| `note` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `line_items[]` | body | `array<object>` | no | — |
| `tax_name` | body | `string` | no | — |
| `tax_rate` | body | `number` | no | — |
