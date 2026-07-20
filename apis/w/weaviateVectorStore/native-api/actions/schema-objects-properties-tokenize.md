# Tokenize text using a property's configuration with Weaviate Vector Store

Tokenizes text using a property's configuration in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/:className/properties/:propertyName/tokenize`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Tokenize text using a property's configuration](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) containing the property. |
| `propertyname` | path | `string` | yes | The name of the property whose tokenization configuration should be used. |
