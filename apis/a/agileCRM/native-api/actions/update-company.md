# Update Company with Agile CRM

Updates an existing company in Agile CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/edit-properties`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Update Company](https://github.com/agilecrm/rest-api#22-updating-a-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `list` | yes |
| `name` | body | `string` | no |
| `url` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
