# List aliases with Weaviate Vector Store

Retrieves aliases from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/aliases`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [List aliases](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `class` | query | `string` | no | Optional filter to retrieve aliases for a specific collection (class) only. If not provided, returns all aliases. |
