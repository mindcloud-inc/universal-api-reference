# List Terms With SEO Metadata with Yoast SEO

Lists taxonomy terms with Yoast SEO metadata.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/:taxonomyRoute`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [List Terms With SEO Metadata](https://developer.yoast.com/customization/apis/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomyRoute` | path | `string` | yes | WordPress REST route for the taxonomy terms collection, such as categories or post_tag. |
| `search` | body | `string` | no | Filter terms by a search string. |
| `slug` | body | `string` | no | Filter terms by slug. |
| `per_page` | body | `number` | no | Number of terms to return per page. |
| `page` | body | `number` | no | Page number to return. |
