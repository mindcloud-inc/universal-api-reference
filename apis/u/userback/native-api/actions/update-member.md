# Update Member with Userback

Updates a Userback member.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/member/:id`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Update Member](https://docs.userback.io/reference/updatemember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The member ID to update. |
| `name` | body | `string` | yes | The updated member name. |
