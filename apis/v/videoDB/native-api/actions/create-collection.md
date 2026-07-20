# Create Collection with VideoDB

Creates a new collection in VideoDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [Create Collection](https://docs.videodb.io/api-reference/collections/create_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Collection name |
| `description` | body | `string` | no | Collection description |
| `is_public` | body | `boolean` | no | Whether the collection is public |
