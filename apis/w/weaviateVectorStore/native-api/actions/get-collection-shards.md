# Get Collection Shards with Weaviate Vector Store

Retrieves the shards status of a collection from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/schema/:className/shards`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get Collection Shards](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `className` | path | `string` | yes | The collection class name. |
