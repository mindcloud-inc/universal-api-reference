# Assign a role to a user with Weaviate Vector Store

Assigns a role to a user in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/authz/users/:id/assign`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Assign a role to a user](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name of the user. |
