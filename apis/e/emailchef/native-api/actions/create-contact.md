# Create Contact with Emailchef

Creates a new contact in Emailchef.

## Endpoint

- **Method:** `POST`
- **Path:** `contacts`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Create Contact](https://emailchef.com/integration/#/Contacts/createContact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `instance_in.list_id` | body | `string` | yes |
| `instance_in.email` | body | `string` | yes |
| `instance_in.status` | body | `string` | no |
| `instance_in.firstname` | body | `string` | no |
| `instance_in.lastname` | body | `string` | no |
