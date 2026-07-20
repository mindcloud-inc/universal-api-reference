# Update User with SweetProcess

Updates an existing teammate in SweetProcess.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:id/`
- **Base URL:** `https://www.sweetprocess.com/api/v1`
- **Official documentation:** [Update User](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric SweetProcess user ID. |
| `name` | body | `string` | no | The teammate's display name. |
| `email` | body | `string` | no | The teammate's email address. |
| `is_super_manager` | body | `boolean` | no | Whether the teammate has super manager access. |
| `is_super_teammate` | body | `boolean` | no | Whether the teammate has super teammate access. |
| `is_billing_admin` | body | `boolean` | no | Whether the teammate has billing admin access. |
