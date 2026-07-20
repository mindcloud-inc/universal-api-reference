# Cancel a replication operation with Weaviate Vector Store

Cancels a replication operation in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/replication/replicate/:id/cancel`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Cancel a replication operation](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the replication operation to cancel. |
