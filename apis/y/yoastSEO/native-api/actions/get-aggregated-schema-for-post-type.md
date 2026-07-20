# Get Aggregated Schema For Post Type with Yoast SEO

Retrieves aggregated schema for a post type.

## Endpoint

- **Method:** `GET`
- **Path:** `/yoast/v1/schema-aggregator/get-schema/:postType/:page`
- **Base URL:** `{siteUrl}/wp-json`
- **Official documentation:** [Get Aggregated Schema For Post Type](https://developer.yoast.com/features/schema/schema-aggregator/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postType` | path | `string` | yes | Post type slug to aggregate, such as post, page, or product. |
| `page` | path | `number` | no | Schema aggregation page number. |
