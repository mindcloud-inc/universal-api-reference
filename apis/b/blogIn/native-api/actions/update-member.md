# Update Member with BlogIn

Updates an existing member in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/:id`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Update Member](https://blogin.co/api/rest/docs/#update-a-specific-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the member to update. |
| `email` | body | `string` | yes | The email address of the member. |
| `username` | body | `string` | yes | The username of the member. |
| `name` | body | `string` | no | The first name of the member. |
| `surname` | body | `string` | no | The surname of the member. |
| `access_level` | body | `string` | no | The access level of the member. |
