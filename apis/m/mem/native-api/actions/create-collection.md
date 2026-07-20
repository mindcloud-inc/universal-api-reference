# Create Collection with Mem

Creates a new collection in Mem.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/collections`
- **Base URL:** `https://api.mem.ai`
- **Official documentation:** [Create Collection](https://docs.mem.ai/api-reference/collections/create-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The collection title. |
| `id` | body | `string` | no | Optional collection ID. |
| `description` | body | `string` | no | — |
| `created_at` | body | `date` | no | — |
| `updated_at` | body | `date` | no | — |
