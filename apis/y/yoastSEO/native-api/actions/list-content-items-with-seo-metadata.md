# List Content Items With SEO Metadata with Yoast SEO

Lists content items with Yoast SEO metadata for a content type.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/:contentType`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [List Content Items With SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | path | `string` | yes | WordPress REST route for the content type, such as posts, pages, or a custom post type route. |
| `search` | body | `string` | no | Filter content items by a search string. |
| `slug` | body | `string` | no | Filter content items by slug. |
| `per_page` | body | `number` | no | Number of items to return per page. |
| `page` | body | `number` | no | Page number to return. |
