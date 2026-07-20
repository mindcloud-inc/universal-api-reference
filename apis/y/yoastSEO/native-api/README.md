# Yoast SEO: Native API Reference

A consolidated summary of Yoast SEO's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://developer.yoast.com/customization/apis/overview/
- **API base URL:** `{siteUrl}/wp-json`

## Authentication

### WordPress Site URL

Provide the base URL of the WordPress site that has the Yoast SEO plugin enabled.

### Credentials

- **Site URL:** `siteUrl` · required · Base URL of the WordPress site, for example https://example.com.

[Official authentication documentation](https://developer.yoast.com/customization/apis/rest-api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Aggregated Schema For Post Type](actions/get-aggregated-schema-for-post-type.md) | `GET /yoast/v1/schema-aggregator/get-schema/:postType/:page` | [docs](https://developer.yoast.com/features/schema/schema-aggregator/api-reference/) |
| [Get Content Item SEO Metadata](actions/get-content-item-seo-metadata.md) | `GET /wp/v2/:contentType/:id` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Content Type SEO Metadata](actions/get-content-type-seo-metadata.md) | `GET /wp/v2/types/:type` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Page SEO Metadata](actions/get-page-seo-metadata.md) | `GET /wp/v2/pages/:id` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Post SEO Metadata](actions/get-post-seo-metadata.md) | `GET /wp/v2/posts/:id` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Schema Aggregator Sitemap XML](actions/get-schema-aggregator-sitemap-xml.md) | `GET /yoast/v1/schema-aggregator/get-xml` | [docs](https://developer.yoast.com/features/schema/schema-aggregator/api-reference/) |
| [Get SEO Head For URL](actions/get-seo-head-for-url.md) | `GET /yoast/v1/get_head` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Site SEO Head](actions/get-site-seo-head.md) | `GET /yoast/v1/get_head` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [Get Taxonomy](actions/get-taxonomy.md) | `GET /wp/v2/taxonomies/:taxonomy` | [docs](https://developer.wordpress.org/rest-api/reference/taxonomies/) |
| [Get Term SEO Metadata](actions/get-term-seo-metadata.md) | `GET /wp/v2/:taxonomyRoute/:id` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [List Content Items With SEO Metadata](actions/list-content-items-with-seo-metadata.md) | `GET /wp/v2/:contentType` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [List Content Types With SEO Metadata](actions/list-content-types-with-seo-metadata.md) | `GET /wp/v2/types` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [List Pages With SEO Metadata](actions/list-pages-with-seo-metadata.md) | `GET /wp/v2/pages` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [List Posts With SEO Metadata](actions/list-posts-with-seo-metadata.md) | `GET /wp/v2/posts` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
| [List Taxonomies](actions/list-taxonomies.md) | `GET /wp/v2/taxonomies` | [docs](https://developer.wordpress.org/rest-api/reference/taxonomies/) |
| [List Terms With SEO Metadata](actions/list-terms-with-seo-metadata.md) | `GET /wp/v2/:taxonomyRoute` | [docs](https://developer.yoast.com/customization/apis/rest-api/) |
