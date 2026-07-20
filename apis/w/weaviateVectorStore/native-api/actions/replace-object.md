# Replace Object with Weaviate Vector Store

Updates an object in Weaviate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/objects/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Replace Object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `class` | query | `string` | no |
| `id` | body | `string` | yes |
| `class` | body | `string` | yes |
| `properties.title` | body | `string` | yes |
| `properties.status` | body | `string` | no |
