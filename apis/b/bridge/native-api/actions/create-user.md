# Create User with Bridge

Creates a user in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/aggregation/users`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create User](https://docs.bridgeapi.io/reference/createuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_user_id` | body | `string` | no | Your own user ID (format: [a-zA-Z0-9-_]{1,128}) |
