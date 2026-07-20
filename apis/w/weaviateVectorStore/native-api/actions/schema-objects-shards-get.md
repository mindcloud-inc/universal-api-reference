# Get the shards status of a collection with Weaviate Vector Store

Retrieves the shards status of a collection from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/schema/:className/shards`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get the shards status of a collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) whose shards to query. |
| `tenant` | query | `string` | no | The name of the tenant for which to retrieve shard statuses (only applicable for multi-tenant collections). |
