# Get Collection with Weaviate Vector Store

Retrieves a single collection from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/schema/:className`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get Collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `className` | path | `string` | yes | The collection class name. |
