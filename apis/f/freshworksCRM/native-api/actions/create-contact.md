# Create Contact with Freshworks CRM

Creates a new contact in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `api/contacts`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Contact](https://developers.freshworks.com/crm/api/#create_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | no | Contact payload object as documented by Freshworks CRM. |
| `contact.address` | body | `string` | no | — |
| `contact.campaign_id` | body | `number` | no | — |
| `contact.city` | body | `string` | no | — |
| `contact.contact_status_id` | body | `number` | no | — |
| `contact.country` | body | `string` | no | — |
| `contact.custom_field` | body | `object` | no | — |
| `contact.custom_field.cf_is_active` | body | `boolean` | no | — |
| `contact.email` | body | `string` | yes | Primary email address. Freshworks rejects contact creation when email is blank. |
| `contact.emails[]` | body | `array<string>` | no | — |
| `contact.external_id` | body | `string` | no | — |
| `contact.facebook` | body | `string` | no | — |
| `contact.first_name` | body | `string` | no | — |
| `contact.job_title` | body | `string` | no | — |
| `contact.keyword` | body | `string` | no | — |
| `contact.last_name` | body | `string` | yes | — |
| `contact.lead_source_id` | body | `number` | no | — |
| `contact.lifecycle_stage_id` | body | `number` | no | — |
| `contact.linkedin` | body | `string` | no | — |
| `contact.medium` | body | `string` | no | — |
| `contact.mobile_number` | body | `string` | no | — |
| `contact.owner_id` | body | `number` | no | — |
| `contact.sales_account_id` | body | `number` | no | — |
| `contact.sales_accounts[]` | body | `array<object>` | no | — |
| `contact.sales_accounts[].id` | body | `number` | no | — |
| `contact.sales_accounts[].is_primary` | body | `boolean` | no | — |
| `contact.state` | body | `string` | no | — |
| `contact.subscription_status[]` | body | `array<string>` | no | — |
| `contact.subscription_types[]` | body | `array<string>` | no | — |
| `contact.territory_id` | body | `number` | no | — |
| `contact.time_zone` | body | `string` | no | — |
| `contact.twitter` | body | `string` | no | — |
| `contact.work_number` | body | `string` | no | — |
| `contact.zipcode` | body | `string` | no | — |
