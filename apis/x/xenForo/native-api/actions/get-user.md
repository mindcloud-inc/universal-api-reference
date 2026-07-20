# Get User with XenForo

Retrieves the specified user from XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get User](https://docs.xenforo.com/api/get-users-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user to retrieve. |
| `with_posts` | query | `boolean` | no | If true, include a page of profile posts with the user response. |
