# Get users assigned to a role with Weaviate Vector Store

Retrieves users assigned to a role from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/authz/roles/:id/user-assignments`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get users assigned to a role](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name (ID) of the role. |
