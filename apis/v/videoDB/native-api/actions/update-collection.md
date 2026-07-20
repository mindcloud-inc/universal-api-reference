# Update Collection with VideoDB

Updates an existing collection in VideoDB.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collection/:collection_id`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [Update Collection](https://docs.videodb.io/api-reference/collections/update_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection ID |
| `name` | body | `string` | no | Updated collection name |
| `description` | body | `string` | no | Updated collection description |
| `is_public` | body | `boolean` | no | Whether the collection is public |
