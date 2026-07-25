# Get groups that have a specific role assigned with Weaviate Vector Store

Retrieves groups that have a specific role assigned from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/authz/roles/:id/group-assignments`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get groups that have a specific role assigned](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique name of the role. |
