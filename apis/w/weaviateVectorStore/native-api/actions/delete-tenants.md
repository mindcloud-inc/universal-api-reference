# Delete Tenants with Weaviate Vector Store

Deletes tenants from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete Tenants](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `className` | path | `string` | yes |
| `tenantNames[0]` | body | `string` | yes |
