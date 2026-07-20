# Get an object with Weaviate Vector Store

Retrieves an object from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get an object](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique UUID of the object to be retrieved. |
| `include` | query | `string` | no | Include additional information, such as classification information. Allowed values include: `classification`, `vector` and `interpretation`. |
