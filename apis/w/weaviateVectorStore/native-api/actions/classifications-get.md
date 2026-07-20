# Get classification status with Weaviate Vector Store

Retrieves classification status from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/classifications/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get classification status](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier (UUID) of the classification task. |
