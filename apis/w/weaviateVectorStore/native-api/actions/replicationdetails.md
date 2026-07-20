# Retrieve a replication operation with Weaviate Vector Store

Retrieve a replication operation in Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/replication/replicate/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Retrieve a replication operation](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the replication operation to get details for. |
| `includeHistory` | query | `string` | no | Whether to include the history of the replication operation. |
