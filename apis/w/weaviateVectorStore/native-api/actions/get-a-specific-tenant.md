# Get a specific tenant with Weaviate Vector Store

Retrieves a specific tenant from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/schema/:className/tenants/:tenantName`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get a specific tenant](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) containing the tenant. |
| `tenantname` | path | `string` | yes | The name of the tenant to retrieve. |
