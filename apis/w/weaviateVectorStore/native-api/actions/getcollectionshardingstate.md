# Get sharding state with Weaviate Vector Store

Retrieves sharding state from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/replication/sharding-state`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get sharding state](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | query | `string` | no | The collection name to get the sharding state for. |
| `shard` | query | `string` | no | The shard to get the sharding state for. |
