# Update User with Rossum

Updates a user in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:userID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update User](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userID` | path | `number` | yes | Rossum user ID. |
| `last_name` | body | `string` | no | Updated user last name. |
