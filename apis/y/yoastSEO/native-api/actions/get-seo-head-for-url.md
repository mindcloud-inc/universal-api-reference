# Get SEO Head For URL with Yoast SEO

Retrieves Yoast SEO metadata for a specific URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/yoast/v1/get_head`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get SEO Head For URL](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Absolute URL to inspect for Yoast SEO metadata. |
