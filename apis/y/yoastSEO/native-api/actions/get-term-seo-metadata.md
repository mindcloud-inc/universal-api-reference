# Get Term SEO Metadata with Yoast SEO

Retrieves Yoast SEO metadata for a taxonomy term.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/:taxonomyRoute/:id`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get Term SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomyRoute` | path | `string` | yes | WordPress REST route for the taxonomy terms collection, such as categories or post_tag. |
| `id` | path | `number` | yes | Numeric ID of the taxonomy term to retrieve. |
