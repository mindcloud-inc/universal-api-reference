# Delete an object with Weaviate Vector Store

Deletes an object from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete an object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique UUID of the object to be deleted. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
