# Add User to Lists with Engage

Adds a user to one or more lists in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:uid/lists`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Add User to Lists](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#add-user-to-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lists[]` | body | `array<string>` | yes | Array of list IDs to add the user to. |
| `uid` | path | `string` | yes | The user ID from your application. |
