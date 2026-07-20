# Create Contact with Sunwise

Creates or updates a contact in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Create Contact](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
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
