# Patch an object with Weaviate Vector Store

Patches an object in Weaviate.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/objects/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Patch an object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique UUID of the object to be patched. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
