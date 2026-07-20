# <img src="https://images.mindcloud.co/apps/icons/data-for-seo_1774043962095.png" alt="DataForSEO logo" width="28" height="28"> DataForSEO: Universal API

Analyze SERPs, keywords, backlinks, and SEO data at scale

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataForSEO/latest
- **Category:** Marketing
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dataforseo.com
- **Vendor API docs:** https://docs.dataforseo.com/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bulk Keyword Difficulty](actions/get-bulk-keyword-difficulty.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty?connectionId=$CONNECTION_ID&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user account data from DataForSEO. |

### Competitor Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Competitor Domains](actions/get-competitor-domains.md) | GET | Retrieves competitor domain data from DataForSEO. |

### Domain Intersection

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Intersection](actions/get-domain-intersection.md) | GET | Retrieves domain intersection data from DataForSEO. |

### Domain Rank Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Rank Overview](actions/get-domain-rank-overview.md) | GET | Retrieves domain rank overview data from DataForSEO. |

### Keyword Difficulty

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Keyword Difficulty](actions/get-bulk-keyword-difficulty.md) | GET | Retrieves bulk keyword difficulty from DataForSEO. |

### Keyword Idea

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Ideas](actions/get-keyword-ideas.md) | GET | Retrieves keyword idea data from DataForSEO. |

### Keyword Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Overview](actions/get-keyword-overview.md) | GET | Retrieves keyword overview data from DataForSEO. |

### Organic Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Organic Search Results](actions/get-organic-search-results.md) | GET | Retrieves organic search results from DataForSEO. |

### Page Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Instant Page Analysis](actions/get-instant-page-analysis.md) | GET | Retrieves instant page analysis from DataForSEO. |

### Page Intersection

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Intersection](actions/get-page-intersection.md) | GET | Retrieves page intersection data from DataForSEO. |

### Ranked Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Ranked Keywords](actions/get-ranked-keywords.md) | GET | Retrieves ranked keyword data from DataForSEO. |

### Relevant Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Relevant Pages](actions/get-relevant-pages.md) | GET | Retrieves relevant pages from DataForSEO. |

### Search Volume

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Volume](actions/get-search-volume.md) | GET | Retrieves keyword search volume from DataForSEO. |

### Site Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Keywords for Site](actions/get-keywords-for-site.md) | GET | Retrieves keywords for a site from DataForSEO. |

### Subdomain

| Action | Method | Description |
| --- | --- | --- |
| [Get Subdomains](actions/get-subdomains.md) | GET | Retrieves subdomain data from DataForSEO. |

### Traffic Estimation

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Traffic Estimation](actions/get-bulk-traffic-estimation.md) | GET | Retrieves bulk traffic estimates from DataForSEO. |

