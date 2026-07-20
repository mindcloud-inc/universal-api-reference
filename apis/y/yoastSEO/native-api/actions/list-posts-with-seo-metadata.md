# List Posts With SEO Metadata with Yoast SEO

Lists posts with Yoast SEO metadata.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [List Posts With SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to posts matching a search string. |
| `slug` | query | `string` | no | Limit results to posts matching an exact slug. |
| `per_page` | query | `number` | no | Maximum number of posts to return per page. |
| `page` | query | `number` | no | Page number of results to return. |
