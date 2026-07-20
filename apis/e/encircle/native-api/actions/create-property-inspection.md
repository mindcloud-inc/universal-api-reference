# Create Property Inspection with Encircle

Creates a property inspection in Encircle.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/property_inspections`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Create Property Inspection](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization_id` | body | `string` | yes |
| `brand_id` | body | `number` | yes |
| `insurer_identifier` | body | `string` | yes |
| `policyholder_name` | body | `string` | no |
| `full_address` | body | `string` | no |
| `policyholder_email_address` | body | `string` | no |
| `policyholder_phone_number` | body | `string` | no |
| `inspection_date` | body | `date` | no |
| `underwriter` | body | `string` | no |
| `inspection_creator` | body | `string` | no |
| `estimated_building_value` | body | `number` | no |
| `insurance_company_name` | body | `string` | no |
| `insurance_broker_name` | body | `string` | no |
| `policy_number` | body | `string` | no |
| `policy_renewal_date` | body | `date` | no |
