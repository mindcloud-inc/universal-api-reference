# Update Company with Keap

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/{company_id}`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Update Company](https://developer.keap.com/docs/restv2/#tag/Company/operation/updateCompany)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | — |
| `company_id` | path | `string` | yes | The unique identifier of the company. |
| `company_name` | body | `string` | no | — |
| `custom_fields` | body | `string` | no | — |
| `email_address` | body | `string` | no | — |
| `fax_number` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `phone_number` | body | `string` | no | — |
| `update_mask` | query | `string` | no | — |
| `website` | body | `string` | no | — |
