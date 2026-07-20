# Create Contact with Agile CRM

Creates a new contact in Agile CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Create Contact](https://github.com/agilecrm/rest-api#13-creating-a-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
| `contact_company_id` | body | `list<number>` | no |
| `lead_score` | body | `number` | no |
| `star_value` | body | `number` | no |
| `tags[]` | body | `array<string>` | no |
