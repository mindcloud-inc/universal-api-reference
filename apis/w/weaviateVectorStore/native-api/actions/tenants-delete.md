# Delete tenants with Weaviate Vector Store

Deletes tenants from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete tenants](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) from which to delete tenants. |
