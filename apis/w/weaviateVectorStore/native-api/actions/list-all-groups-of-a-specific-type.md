# List all groups of a specific type with Weaviate Vector Store

Retrieves all groups of a specific type from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/authz/groups/:groupType`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [List all groups of a specific type](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grouptype` | path | `string` | yes | The type of group to retrieve. |
