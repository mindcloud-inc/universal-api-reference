# DataForSEO: Native API Reference

A consolidated summary of DataForSEO's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.dataforseo.com/v3/
- **API base URL:** `https://api.dataforseo.com`

## Authentication

### API Login + Password

Enter your DataForSEO API login in Username and your API password in Password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.dataforseo.com/v3/auth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the request body to set the page size. Use `offset` in the request body as the record offset; numbering starts at 0.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bulk Keyword Difficulty](actions/get-bulk-keyword-difficulty.md) | `POST /v3/dataforseo_labs/bulk_keyword_difficulty/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-bulk_keyword_difficulty-live/) |
| [Get Bulk Traffic Estimation](actions/get-bulk-traffic-estimation.md) | `POST /v3/dataforseo_labs/bulk_traffic_estimation/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-bulk_traffic_estimation-live/) |
| [Get Competitor Domains](actions/get-competitor-domains.md) | `POST /v3/dataforseo_labs/google/competitors_domain/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-competitors_domain-live/) |
| [Get Domain Intersection](actions/get-domain-intersection.md) | `POST /v3/dataforseo_labs/google/domain_intersection/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-domain_intersection-live/) |
| [Get Domain Rank Overview](actions/get-domain-rank-overview.md) | `POST /v3/dataforseo_labs/google/domain_rank_overview/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-domain_rank_overview-live/) |
| [Get Instant Page Analysis](actions/get-instant-page-analysis.md) | `POST /v3/on_page/instant_pages.ai` | [docs](https://docs.dataforseo.com/v3/on_page-instant_pages/) |
| [Get Keyword Ideas](actions/get-keyword-ideas.md) | `POST /v3/dataforseo_labs/google/keyword_ideas/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_ideas-live/) |
| [Get Keyword Overview](actions/get-keyword-overview.md) | `POST /v3/dataforseo_labs/google/keyword_overview/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_overview-live/) |
| [Get Keywords for Site](actions/get-keywords-for-site.md) | `POST /v3/dataforseo_labs/google/keywords_for_site/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-keywords_for_site-live/) |
| [Get Organic Search Results](actions/get-organic-search-results.md) | `POST /v3/serp/:search_engine/organic/live/advanced.ai` | [docs](https://docs.dataforseo.com/v3/serp-se-type-live-advanced/) |
| [Get Page Intersection](actions/get-page-intersection.md) | `POST /v3/dataforseo_labs/google/page_intersection/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-page_intersection-live/) |
| [Get Ranked Keywords](actions/get-ranked-keywords.md) | `POST /v3/dataforseo_labs/google/ranked_keywords/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-ranked_keywords-live/) |
| [Get Relevant Pages](actions/get-relevant-pages.md) | `POST /v3/dataforseo_labs/google/relevant_pages/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-relevant_pages-live/) |
| [Get Search Volume](actions/get-search-volume.md) | `POST /v3/keywords_data/google_ads/search_volume/live.ai` | [docs](https://docs.dataforseo.com/v3/keywords_data-google_ads-search_volume-live/) |
| [Get Subdomains](actions/get-subdomains.md) | `POST /v3/dataforseo_labs/google/subdomains/live.ai` | [docs](https://docs.dataforseo.com/v3/dataforseo_labs-google-subdomains-live/) |
| [Get User Data](actions/get-user-data.md) | `GET /v3/appendix/user_data` | [docs](https://docs.dataforseo.com/v3/appendix-user-data/) |
