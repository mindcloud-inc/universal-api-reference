# Replace Study User Roles with Castor EDC

Updates study user roles in Castor EDC.

## Endpoint

- **Method:** `PUT`
- **Path:** `/study/:study_id/user/:user_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Replace Study User Roles](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `user_id` | path | `string` | yes | The study user UUID. |
| `manage_permissions` | body | `object` | no | Management permission flags as an object. |
| `role_assignments[]` | body | `array<object>` | no | Array of role assignment objects with site_id and role_name. |
| `default_role_assignment` | body | `number` | no | Default site role identifier. |
