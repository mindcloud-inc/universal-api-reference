# Create Collection with Chroma Vector Store

Creates a new collection in Chroma.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create Collection](https://docs.trychroma.com/reference/chroma-api/collection/create-collection)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `database` | path | `string` | yes |
| `name` | body | `string` | yes |
| `tenant` | path | `string` | yes |
