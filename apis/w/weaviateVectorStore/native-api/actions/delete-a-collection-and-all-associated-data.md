# Delete a collection (and all associated data) with Weaviate Vector Store

Deletes a collection (and all associated data) from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/schema/:className`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete a collection (and all associated data)](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) to delete. |
