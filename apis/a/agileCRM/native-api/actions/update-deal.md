# Update Deal with Agile CRM

Updates an existing deal in Agile CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/opportunity/partial-update`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Update Deal](https://github.com/agilecrm/rest-api#34-update-deal-partial-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `list` | yes |
| `name` | body | `string` | no |
| `expected_value` | body | `number` | no |
| `milestone` | body | `string` | no |
