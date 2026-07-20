# Create collection with Chroma Cloud

Creates a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create collection](https://docs.trychroma.com/reference/chroma-api/collection/create-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `get_or_create` | body | `boolean` | no | Return an existing collection with this name when one exists. |
| `metadata` | body | `object` | no | Optional collection metadata object. |
