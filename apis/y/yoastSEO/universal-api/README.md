# <img src="https://images.mindcloud.co/apps/icons/yoast-seo_1776270434011.png" alt="Yoast SEO logo" width="28" height="28"> Yoast SEO: Universal API

Retrieve Yoast SEO metadata, Yoast-enriched WordPress REST responses for content types and taxonomies, and Schema Aggregator outputs for WordPress sites running Yoast SEO.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yoastSEO/latest
- **Category:** Website & App Building / CMS
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yoast.com/
- **Vendor API docs:** https://developer.yoast.com/customization/apis/overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Content Types With SEO Metadata](actions/list-content-types-with-seo-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-types-with-seo-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Schema For Post Type](actions/get-aggregated-schema-for-post-type.md) | GET | Retrieves aggregated schema for a post type. |
| [Get Content Item SEO Metadata](actions/get-content-item-seo-metadata.md) | GET | Retrieves Yoast SEO metadata for a content item. |
| [Get Post SEO Metadata](actions/get-post-seo-metadata.md) | GET | Retrieves Yoast SEO metadata for a post. |
| [List Content Items With SEO Metadata](actions/list-content-items-with-seo-metadata.md) | GET | Lists content items with Yoast SEO metadata for a content type. |
| [List Posts With SEO Metadata](actions/list-posts-with-seo-metadata.md) | GET | Lists posts with Yoast SEO metadata. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Type SEO Metadata](actions/get-content-type-seo-metadata.md) | GET | Retrieves Yoast SEO metadata for a content type archive. |
| [Get Schema Aggregator Sitemap XML](actions/get-schema-aggregator-sitemap-xml.md) | GET | Retrieves the Schema Aggregator sitemap XML. |
| [Get Taxonomy](actions/get-taxonomy.md) | GET | Retrieves a WordPress taxonomy. |
| [List Content Types With SEO Metadata](actions/list-content-types-with-seo-metadata.md) | GET | Lists content types with Yoast SEO metadata. |
| [List Taxonomies](actions/list-taxonomies.md) | GET | Lists WordPress taxonomies. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Page SEO Metadata](actions/get-page-seo-metadata.md) | GET | Retrieves Yoast SEO metadata for a page. |
| [Get SEO Head For URL](actions/get-seo-head-for-url.md) | GET | Retrieves Yoast SEO metadata for a specific URL. |
| [Get Site SEO Head](actions/get-site-seo-head.md) | GET | Retrieves Yoast SEO metadata for the connected site URL. |
| [List Pages With SEO Metadata](actions/list-pages-with-seo-metadata.md) | GET | Lists pages with Yoast SEO metadata. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Term SEO Metadata](actions/get-term-seo-metadata.md) | GET | Retrieves Yoast SEO metadata for a taxonomy term. |
| [List Terms With SEO Metadata](actions/list-terms-with-seo-metadata.md) | GET | Lists taxonomy terms with Yoast SEO metadata. |

