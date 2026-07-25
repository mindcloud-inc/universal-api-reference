# Replace object references with Weaviate Vector Store

Replaces object references in Weaviate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/:id/references/:propertyName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Replace object references](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique UUID of the source object. |
| `propertyname` | path | `string` | yes | Unique name of the reference property of the source object. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
