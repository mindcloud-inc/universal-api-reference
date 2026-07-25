# Get the list of tenants with Weaviate Vector Store

Retrieves the list of tenants from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/schema/:className/tenants`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get the list of tenants](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) whose tenants to list. |
