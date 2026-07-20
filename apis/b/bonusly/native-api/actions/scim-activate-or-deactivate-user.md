# SCIM Activate Or Deactivate User with Bonusly

Activates or deactivates a SCIM user in Bonusly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://bonus.ly/api/scim11/Users/:id`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [SCIM Activate Or Deactivate User](https://docs.bonus.ly/reference/activate-or-deactivate-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The SCIM user ID. |
