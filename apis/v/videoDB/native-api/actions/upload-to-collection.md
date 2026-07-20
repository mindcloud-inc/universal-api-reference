# Upload to Collection with VideoDB

Uploads media to a collection in VideoDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/:collection_id/upload`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [Upload to Collection](https://docs.videodb.io/api-reference/collections/upload_to_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection ID to upload into |
| `url` | body | `string` | yes | Public media URL to ingest |
| `name` | body | `string` | no | Name for the uploaded media |
| `media_type` | body | `string` | no | Media type such as video |
| `callback_url` | body | `string` | no | Optional callback URL |
