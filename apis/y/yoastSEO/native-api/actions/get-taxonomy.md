# Get Taxonomy with Yoast SEO

Retrieves a WordPress taxonomy.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/taxonomies/:taxonomy`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get Taxonomy](https://developer.wordpress.org/rest-api/reference/taxonomies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomy` | path | `string` | yes | Taxonomy slug to retrieve, such as category or post_tag. |
