# Update Property Inspection with Encircle

Updates a property inspection in Encircle.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/property_inspections/:property_inspection_id`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Update Property Inspection](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_inspections~1{property_inspection_id}/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `property_inspection_id` | path | `number` | yes |
| `insurer_identifier` | body | `string` | no |
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
