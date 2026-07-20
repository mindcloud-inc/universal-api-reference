# Get Podcast Subcategory with Simplecast

Retrieves a podcast subcategory from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/categories/:category_id/subcategories/:subcategory_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Podcast Subcategory](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `string` | yes | Simplecast category identifier. |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
| `subcategory_id` | path | `string` | yes | Simplecast subcategory identifier. |
