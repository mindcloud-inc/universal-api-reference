# Add Tenants with Weaviate Vector Store

Creates a new tenant in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add Tenants](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `className` | path | `string` | yes |
| `tenants[0].name` | body | `string` | yes |
| `tenants[0].activityStatus` | body | `string` | no |
