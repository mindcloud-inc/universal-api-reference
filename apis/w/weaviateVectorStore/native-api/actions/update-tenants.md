# Update Tenants with Weaviate Vector Store

Updates a tenant in Weaviate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Update Tenants](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `className` | path | `string` | yes |
| `tenants[0].name` | body | `string` | yes |
| `tenants[0].activityStatus` | body | `string` | yes |
