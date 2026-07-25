# Get an object with Weaviate Vector Store

Retrieves an object from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/:className/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get an object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | Name of the collection (class) the object belongs to. |
| `id` | path | `string` | yes | Unique UUID of the object to be retrieved. |
| `include` | query | `string` | no | Include additional information, such as classification information. Allowed values include: `classification`, `vector` and `interpretation`. |
| `consistency_level` | query | `string` | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `node_name` | query | `string` | no | The target node which should fulfill the request. |
| `tenant` | query | `string` | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |
