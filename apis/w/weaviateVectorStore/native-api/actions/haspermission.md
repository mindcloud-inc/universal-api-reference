# Check whether a role possesses a permission with Weaviate Vector Store

Checks whether a role possesses a permission in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/authz/roles/:id/has-permission`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Check whether a role possesses a permission](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The name of the role. |
