# Delete a collection's vector index. with Weaviate Vector Store

Deletes a collection's vector index from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/schema/:className/vectors/:vectorIndexName/index`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete a collection's vector index.](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) containing the property. |
| `vectorindexname` | path | `string` | yes | The name of the vector index. |
