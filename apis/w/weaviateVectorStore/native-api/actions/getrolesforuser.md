# Get roles assigned to a user with Weaviate Vector Store

Retrieves roles assigned to a user from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/authz/users/:id/roles/:userType`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get roles assigned to a user](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name of the user. |
| `usertype` | path | `string` | yes | The type of the user. |
| `includeFullRoles` | query | `string` | no | Whether to include detailed role information like its assigned permissions. |
