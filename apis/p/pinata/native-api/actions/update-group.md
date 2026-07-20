# Update Group with Pinata

Updates an existing group in Pinata.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/groups/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Update Group](https://docs.pinata.cloud/api-reference/endpoint/update-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target group. |
| `name` | body | `string` | no | Updated name for the group. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
