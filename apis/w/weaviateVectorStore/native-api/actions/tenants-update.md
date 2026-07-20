# Update a tenant with Weaviate Vector Store

Updates a tenant in Weaviate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Update a tenant](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) containing the tenants. |
