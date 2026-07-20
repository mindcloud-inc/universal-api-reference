# Update User with Edoobox

Updates an existing user in Edoobox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/:user_id`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Update User](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | edoobox user ID. |
| `first_name` | body | `string` | no | Updated user first name. |
| `last_name` | body | `string` | no | Updated user last name. |
| `master` | body | `boolean` | no | Whether the user is a master user. |
