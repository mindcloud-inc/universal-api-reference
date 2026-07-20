# Get replication scale plan with Weaviate Vector Store

Retrieves replication scale plan from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/replication/scale`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get replication scale plan](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | query | `string` | yes | The collection name to get the scaling plan for. |
| `replicationFactor` | query | `string` | yes | The desired replication factor to scale to. Must be a positive integer greater than zero. |
