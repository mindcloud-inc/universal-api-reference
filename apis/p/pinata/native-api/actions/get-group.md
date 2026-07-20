# Get Group with Pinata

Retrieves a group from Pinata by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Group](https://docs.pinata.cloud/api-reference/endpoint/get-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target group. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
