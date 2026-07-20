# Get User with MantisBT

Retrieves a user from MantisBT by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get User](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user to retrieve |
