# Create Objects Batch with Weaviate Vector Store

Creates objects in batch in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/objects`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Create Objects Batch](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `objects[0].class` | body | `string` | yes |
| `objects[0].properties.title` | body | `string` | yes |
| `objects[0].properties.status` | body | `string` | no |
