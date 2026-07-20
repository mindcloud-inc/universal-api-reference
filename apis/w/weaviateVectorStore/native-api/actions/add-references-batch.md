# Add References Batch with Weaviate Vector Store

Creates cross-references in bulk in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/references`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Add References Batch](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `references[0].from` | body | `string` | yes |
| `references[0].to` | body | `string` | yes |
