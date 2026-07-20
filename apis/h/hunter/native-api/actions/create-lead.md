# Create Lead with Hunter

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Create Lead](https://hunter.io/api-documentation/v2#create-lead)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `position` | body | `string` | no |
| `company` | body | `string` | no |
| `company_industry` | body | `string` | no |
| `company_size` | body | `string` | no |
| `confidence_score` | body | `number` | no |
| `website` | body | `string` | no |
| `country_code` | body | `string` | no |
| `linkedin_url` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `twitter` | body | `string` | no |
| `notes` | body | `string` | no |
| `source` | body | `string` | no |
| `leads_list_id` | body | `string` | no |
| `leads_list_ids` | body | `list<string>` | no |
