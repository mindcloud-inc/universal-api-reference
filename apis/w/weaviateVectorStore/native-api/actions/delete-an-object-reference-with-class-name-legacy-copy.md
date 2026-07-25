# Delete an Object Reference with Class Name (Legacy Copy) with Weaviate Vector Store

Deletes an object reference from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/:className/:id/references/:propertyName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete an Object Reference with Class Name (Legacy Copy)](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | Name of the collection (class) the source object belongs to. |
| `id` | path | `string` | yes | Unique UUID of the source object. |
| `propertyname` | path | `string` | yes | Unique name of the reference property of the source object. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
