# List replication operations with Weaviate Vector Store

Retrieves replication operations from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/replication/replicate/list`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [List replication operations](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetNode` | query | `string` | no | The name of the target node to get details for. |
| `collection` | query | `string` | no | The name of the collection to get details for. |
| `shard` | query | `string` | no | The shard to get details for. |
| `includeHistory` | query | `string` | no | Whether to include the history of the replication operation. |
