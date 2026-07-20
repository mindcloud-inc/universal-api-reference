# Update Object with Weaviate Vector Store

Patches an object in Weaviate.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/objects/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Update Object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `class` | body | `string` | yes |
| `class` | query | `string` | no |
| `properties.title` | body | `string` | no |
| `properties.status` | body | `string` | no |
