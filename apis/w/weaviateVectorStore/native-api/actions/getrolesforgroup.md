# Get roles assigned to a specific group with Weaviate Vector Store

Retrieves roles assigned to a specific group from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/authz/groups/:id/roles/:groupType`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get roles assigned to a specific group](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique name of the group. |
| `grouptype` | path | `string` | yes | The type of the group. |
| `includeFullRoles` | query | `string` | no | If true, the response will include the full role definitions with all associated permissions. If false, only role names are returned. |
