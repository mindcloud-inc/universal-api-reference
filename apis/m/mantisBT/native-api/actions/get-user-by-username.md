# Get User By Username with MantisBT

Finds a user in MantisBT by username.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/username/{username}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get User By Username](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username of the user to retrieve |
