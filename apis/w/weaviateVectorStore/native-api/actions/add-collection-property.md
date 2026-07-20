# Add Collection Property with Weaviate Vector Store

Adds a property to a collection in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/schema/:className/properties`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add Collection Property](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `className` | path | `string` | yes | The collection class name to update. |
| `dataType[0]` | body | `string` | yes | The property data type to add. |
| `name` | body | `string` | yes | The property name to add. |
