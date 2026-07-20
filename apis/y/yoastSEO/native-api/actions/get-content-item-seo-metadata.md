# Get Content Item SEO Metadata with Yoast SEO

Retrieves Yoast SEO metadata for a content item.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/:contentType/:id`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get Content Item SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | path | `string` | yes | WordPress REST route for the content type, such as posts, pages, or a custom post type route. |
| `id` | path | `number` | yes | Numeric ID of the content item to retrieve. |
