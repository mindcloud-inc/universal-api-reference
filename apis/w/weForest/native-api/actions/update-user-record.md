# Update user record with WeForest

Updates an existing user in WeForest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:id`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Update user record](https://docs.weforest.org/update-user-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated email for the user. |
| `firstName` | body | `string` | no | Updated first name for the user. |
| `id` | path | `number` | yes | User identifier from WeForest. |
| `lastName` | body | `string` | no | Updated last name for the user. |
