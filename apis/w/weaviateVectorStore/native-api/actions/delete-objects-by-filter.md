# Delete Objects By Filter with Weaviate Vector Store

Deletes objects in batch from Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/batch/objects`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Delete Objects By Filter](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `match.class` | body | `string` | yes |
| `match.where.path[0]` | body | `string` | yes |
| `match.where.operator` | body | `string` | yes |
| `match.where.valueText` | body | `string` | yes |
| `output` | body | `string` | no |
| `dryRun` | body | `boolean` | no |
