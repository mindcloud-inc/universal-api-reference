# SCIM Update User with Bonusly

Updates an existing SCIM user in Bonusly.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://bonus.ly/api/scim11/Users/:id`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [SCIM Update User](https://docs.bonus.ly/reference/update-an-existing-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The SCIM user ID. |
| `userName` | body | `string` | yes | SCIM username for the user resource. |
