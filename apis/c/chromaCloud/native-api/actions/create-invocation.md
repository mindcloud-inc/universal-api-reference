# Create invocation with Chroma Cloud

Creates an invocation in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `https://sync.trychroma.com/api/v1/sources/:source_id/invocations`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create invocation](https://docs.trychroma.com/reference/sync-api/invocation/create-invocation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_id` | path | `string` | yes |
| `target_collection_name` | body | `string` | no |
| `object_key` | body | `string` | no |
| `custom_id` | body | `string` | no |
| `metadata` | body | `object` | no |
| `ref_identifier` | body | `object` | no |
