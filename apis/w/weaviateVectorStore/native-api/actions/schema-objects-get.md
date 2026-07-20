# Get a single collection with Weaviate Vector Store

Retrieves a single collection from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/schema/:className`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get a single collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) to retrieve. |
