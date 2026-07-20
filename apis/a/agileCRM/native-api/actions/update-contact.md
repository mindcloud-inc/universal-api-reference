# Update Contact with Agile CRM

Updates an existing contact in Agile CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/edit-properties`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Update Contact](https://github.com/agilecrm/rest-api#14-update-properties-of-a-contact-by-id-partial-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `list` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `email` | body | `string` | no |
