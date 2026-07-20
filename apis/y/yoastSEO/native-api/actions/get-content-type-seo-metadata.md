# Get Content Type SEO Metadata with Yoast SEO

Retrieves Yoast SEO metadata for a content type archive.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/types/:type`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get Content Type SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | WordPress post type key, for example post or page. |
