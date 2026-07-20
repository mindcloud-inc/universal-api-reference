# Create a new tenant with Weaviate Vector Store

Creates a new tenant in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Create a new tenant](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the multi-tenant enabled collection (class). |
