# Get a user by external ID with WorkOS

Retrieves a user by external ID from your WorkOS environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/user_management/users/external_id/{external_id}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Get a user by external ID](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | path | `string` | yes | The external ID of the user. |
