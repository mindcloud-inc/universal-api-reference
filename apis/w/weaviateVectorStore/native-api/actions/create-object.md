# Create Object with Weaviate Vector Store

Creates an object in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/objects`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Create Object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `class` | body | `string` | yes |
| `properties.title` | body | `string` | yes |
| `properties.status` | body | `string` | no |
