# Update a user with Worksnaps

Updates an existing user in Worksnaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{user_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Update a user](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `user_id` | path | `string` | no | ID of the target user |
