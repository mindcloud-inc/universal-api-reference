# Update Company with Freshdesk

Updates an existing company in Freshdesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:id`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Update Company](https://developers.freshdesk.com/api/#update_company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk company ID. |
| `custom_fields` | body | `object` | no | Key-value pairs for custom company fields |
| `description` | body | `string` | no | Description of the company |
| `domains[]` | body | `array<string>` | no | Domains associated with the company |
| `name` | body | `string` | no | Name of the company |
| `note` | body | `string` | no | Specific note about the company |
| `health_score` | body | `string` | no | Relationship strength with the company |
| `account_tier` | body | `string` | no | Business value classification tier |
| `renewal_date` | body | `date` | no | Contract or relationship renewal date |
| `industry` | body | `string` | no | Industry the company serves in |
| `lookup_parameter` | body | `string` | no | Lookup field value for custom object linkage |
