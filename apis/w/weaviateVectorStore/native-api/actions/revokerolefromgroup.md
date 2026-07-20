# Revoke a role from a group with Weaviate Vector Store

Revokes a role from a group in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/authz/groups/:id/revoke`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Revoke a role from a group](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name of the group. |
