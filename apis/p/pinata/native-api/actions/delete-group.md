# Delete Group with Pinata

Deletes an existing group from Pinata.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/groups/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Delete Group](https://docs.pinata.cloud/api-reference/endpoint/delete-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target group. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
