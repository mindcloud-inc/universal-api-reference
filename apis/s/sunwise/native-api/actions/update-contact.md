# Update Contact with Sunwise

Updates an existing contact in Sunwise.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id/`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Update Contact](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `emails` | body | `object` | yes |
| `telephones` | body | `object` | yes |
| `first_lastname` | body | `string` | no |
| `second_lastname` | body | `string` | no |
| `integration_source` | body | `string` | no |
| `status_flag` | body | `string` | no |
| `agent` | body | `string` | no |
| `company_name` | body | `string` | no |
| `contact_origin` | body | `string` | no |
| `status_contact` | body | `string` | no |
