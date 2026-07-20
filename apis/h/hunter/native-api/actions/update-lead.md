# Update Lead with Hunter

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:leadId`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Update Lead](https://hunter.io/api-documentation/v2#update-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | Identifier of the lead. |
| `email` | body | `string` | no | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `position` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `company_industry` | body | `string` | no | — |
| `company_size` | body | `string` | no | — |
| `confidence_score` | body | `number` | no | — |
| `website` | body | `string` | no | — |
| `country_code` | body | `string` | no | — |
| `linkedin_url` | body | `string` | no | — |
| `phone_number` | body | `string` | no | — |
| `twitter` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `source` | body | `string` | no | — |
| `leads_list_id` | body | `string` | no | — |
| `leads_list_ids` | body | `list<string>` | no | — |
