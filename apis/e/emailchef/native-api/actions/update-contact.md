# Update Contact with Emailchef

Updates an existing contact in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `contacts/:contact_id`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Update Contact](https://emailchef.com/integration/#/Contacts/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The Emailchef contact ID. |
| `instance_in.list_id` | body | `string` | yes | — |
| `instance_in.status` | body | `string` | no | — |
| `instance_in.firstname` | body | `string` | no | — |
| `instance_in.lastname` | body | `string` | no | — |
