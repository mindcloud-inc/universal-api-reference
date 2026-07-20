# Update Group with Seven

Updates an existing group in Seven.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:id`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Update Group](https://docs.seven.io/en/rest-api/endpoints/groups#update-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The name of the group. |
| `id` | path | `number` | yes | — |
