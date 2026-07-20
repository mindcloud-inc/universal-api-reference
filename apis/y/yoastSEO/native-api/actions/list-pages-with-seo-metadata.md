# List Pages With SEO Metadata with Yoast SEO

Lists pages with Yoast SEO metadata.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/pages`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [List Pages With SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to pages matching a search string. |
| `slug` | query | `string` | no | Limit results to pages matching an exact slug. |
| `per_page` | query | `number` | no | Maximum number of pages to return per page. |
| `page` | query | `number` | no | Page number of results to return. |
