# Create Company with Freshdesk

Creates a new company in Freshdesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Create Company](https://developers.freshdesk.com/api/#create_company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_fields` | body | `object` | no | Key-value pairs for custom company fields |
| `description` | body | `string` | no | Description of the company |
| `domains[]` | body | `array<string>` | no | Domains associated with the company |
| `name` | body | `string` | yes | Name of the company |
| `note` | body | `string` | no | Specific note about the company |
| `health_score` | body | `string` | no | Relationship strength with the company |
| `account_tier` | body | `string` | no | Business value classification tier |
| `renewal_date` | body | `date` | no | Contract or relationship renewal date |
| `industry` | body | `string` | no | Industry the company serves in |
| `lookup_parameter` | body | `string` | no | Lookup field value for custom object linkage |
