# Delete an object reference with Weaviate Vector Store

Deletes an object reference from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/:id/references/:propertyName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete an object reference](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique UUID of the source object. |
| `propertyname` | path | `string` | yes | Unique name of the reference property of the source object. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
