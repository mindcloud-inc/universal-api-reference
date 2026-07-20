# Update Contact with Keap

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{contact_id}`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Update Contact](https://developer.keap.com/docs/restv2/#tag/Contact/operation/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses` | body | `string` | no | — |
| `anniversary_date` | body | `string` | no | — |
| `birth_date` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `contact_id` | path | `string` | yes | The unique identifier of the contact. |
| `contact_type` | body | `string` | no | — |
| `custom_fields` | body | `string` | no | — |
| `email_addresses` | body | `string` | no | — |
| `family_name` | body | `string` | no | — |
| `fax_numbers` | body | `string` | no | — |
| `fields` | query | `string` | no | — |
| `given_name` | body | `string` | no | — |
| `job_title` | body | `string` | no | — |
| `leadsource_id` | body | `string` | no | — |
| `middle_name` | body | `string` | no | — |
| `origin` | body | `string` | no | — |
| `owner_id` | body | `string` | no | — |
| `phone_numbers` | body | `string` | no | — |
| `preferred_locale` | body | `string` | no | — |
| `preferred_name` | body | `string` | no | — |
| `prefix` | body | `string` | no | — |
| `referral_code` | body | `string` | no | — |
| `social_accounts` | body | `string` | no | — |
| `source_type` | body | `string` | no | — |
| `spouse_name` | body | `string` | no | — |
| `suffix` | body | `string` | no | — |
| `time_zone` | body | `string` | no | — |
| `update_mask` | query | `string` | no | — |
| `utm_parameters` | body | `string` | no | — |
| `website` | body | `string` | no | — |
