# Remove permissions from a role with Weaviate Vector Store

Removes permissions from a role in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/authz/roles/:id/remove-permissions`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Remove permissions from a role](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name of the role being modified. |
