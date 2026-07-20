# List Podcast Subcategories with Simplecast

Retrieves podcast subcategories from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/categories/:category_id/subcategories`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Subcategories](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `string` | yes | Simplecast category identifier. |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
