# Delete a property's inverted index with Weaviate Vector Store

Deletes a property's inverted index from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/schema/:className/properties/:propertyName/index/:indexName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete a property's inverted index](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) containing the property. |
| `propertyname` | path | `string` | yes | The name of the property whose inverted index should be deleted. |
| `indexname` | path | `string` | yes | The name of the inverted index to delete from the property. |
