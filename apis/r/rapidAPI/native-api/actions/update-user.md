# Update User with RapidAPI

Updates an existing user in RapidAPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{userId}`
- **Base URL:** `{baseUrlRest}`
- **Official documentation:** [Update User](https://docs.rapidapi.com/docs/on-behalf-of)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | RapidAPI user ID to update. |
| `email` | body | `string` | no | Updated email address. |
| `name` | body | `string` | no | Updated display name. |
| `username` | body | `string` | no | Updated username. |
| `password` | body | `string` | no | Updated password. |
