# Add an object reference with Weaviate Vector Store

Adds an object reference in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/objects/:className/:id/references/:propertyName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add an object reference](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | Name of the collection (class) the source object belongs to. |
| `id` | path | `string` | yes | Unique UUID of the source object. |
| `propertyname` | path | `string` | yes | Unique name of the reference property of the source object. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
