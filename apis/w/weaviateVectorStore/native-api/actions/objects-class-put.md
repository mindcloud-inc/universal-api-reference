# Replace an object with Weaviate Vector Store

Replaces an object in Weaviate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/:className/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Replace an object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | Name of the collection (class) the object belongs to. |
| `id` | path | `string` | yes | Unique UUID of the object to be replaced. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
