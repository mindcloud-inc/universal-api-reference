# Add a property to a collection with Weaviate Vector Store

Adds a property to a collection in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/:className/properties`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add a property to a collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) to add the property to. |
