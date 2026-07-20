# Create Collection with Weaviate Vector Store

Creates a new collection in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/schema`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Create Collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `class` | body | `string` | yes | The collection class name to create. |
| `multiTenancyConfig.enabled` | body | `boolean` | no | Whether multi-tenancy is enabled. |
| `properties[0].dataType[0]` | body | `string` | yes | The first property data type. |
| `properties[0].name` | body | `string` | yes | The first property name to create. |
| `vectorizer` | body | `string` | yes | The vectorizer for the collection. |
