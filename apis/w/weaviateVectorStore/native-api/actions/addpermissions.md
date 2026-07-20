# Add permissions to a role with Weaviate Vector Store

Adds permissions to a role in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/authz/roles/:id/add-permissions`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add permissions to a role](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name (ID) of the role being modified. |
