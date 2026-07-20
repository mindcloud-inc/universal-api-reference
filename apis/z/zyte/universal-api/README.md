# <img src="https://images.mindcloud.co/apps/icons/zyte-icon_1775148154854.png" alt="Zyte logo" width="28" height="28"> Zyte: Universal API

Access Zyte Stats API reports through curated analytics actions over the official stats endpoint.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zyte/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zyte.com/
- **Vendor API docs:** https://docs.zyte.com/zyte-api/usage/stats.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage Overview](actions/get-usage-overview.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-usage-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Actions Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Actions Feature Usage](actions/get-actions-feature-usage.md) | GET | Retrieves actions feature usage metrics from Zyte. |

### Article Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Article Extraction Usage](actions/get-article-extraction-usage.md) | GET | Retrieves article extraction usage metrics from Zyte. |

### Article List Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Article List Extraction Usage](actions/get-article-list-extraction-usage.md) | GET | Retrieves article list extraction usage metrics from Zyte. |

### Article Navigation Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Article Navigation Extraction Usage](actions/get-article-navigation-extraction-usage.md) | GET | Retrieves article navigation extraction usage metrics from Zyte. |

### Browser Html Extraction Source Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser HTML Extraction Source Usage](actions/get-browser-html-extraction-source-usage.md) | GET | Retrieves article extraction usage metrics from Browser HTML in Zyte. |

### Browser Html Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser HTML Feature Usage](actions/get-browser-html-feature-usage.md) | GET | Retrieves Browser HTML feature usage metrics from Zyte. |

### Daily Domain Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Domain Usage Trend](actions/get-daily-domain-usage-trend.md) | GET | Retrieves daily usage trends grouped by domain from Zyte. |

### Daily Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Usage Trend](actions/get-daily-usage-trend.md) | GET | Retrieves daily usage trends from Zyte. |

### Domain Health Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Health Breakdown](actions/get-domain-health-breakdown.md) | GET | Retrieves domain health metrics grouped by domain from Zyte. |

### Domain Usage Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Usage Breakdown](actions/get-domain-usage-breakdown.md) | GET | Retrieves usage metrics grouped by domain from Zyte. |

### Extended Geolocation Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Extended Geolocation Feature Usage](actions/get-extended-geolocation-feature-usage.md) | GET | Retrieves extended geolocation feature usage metrics from Zyte. |

### File Download Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get File Download Feature Usage](actions/get-file-download-feature-usage.md) | GET | Retrieves file download feature usage metrics from Zyte. |

### Forum Thread Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Forum Thread Extraction Usage](actions/get-forum-thread-extraction-usage.md) | GET | Retrieves forum thread extraction usage metrics from Zyte. |

### Hourly Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Hourly Usage Trend](actions/get-hourly-usage-trend.md) | GET | Retrieves hourly usage trends from Zyte. |

### Http Response Body Extraction Source Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get HTTP Response Body Extraction Source Usage](actions/get-http-response-body-extraction-source-usage.md) | GET | Retrieves article extraction usage metrics from HTTP response body in Zyte. |

### Http Response Body Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get HTTP Response Body Feature Usage](actions/get-http-response-body-feature-usage.md) | GET | Retrieves HTTP response body feature usage metrics from Zyte. |

### Job Posting Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Posting Extraction Usage](actions/get-job-posting-extraction-usage.md) | GET | Retrieves job posting extraction usage metrics from Zyte. |

### Job Posting Navigation Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Posting Navigation Extraction Usage](actions/get-job-posting-navigation-extraction-usage.md) | GET | Retrieves job posting navigation extraction usage metrics from Zyte. |

### Monthly Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Usage Trend](actions/get-monthly-usage-trend.md) | GET | Retrieves monthly usage trends from Zyte. |

### Network Capture Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Capture Feature Usage](actions/get-network-capture-feature-usage.md) | GET | Retrieves network capture feature usage metrics from Zyte. |

### Not Found Response Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Not Found Response Usage](actions/get-not-found-response-usage.md) | GET | Retrieves 404 response usage metrics from Zyte. |

### Product Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Extraction Usage](actions/get-product-extraction-usage.md) | GET | Retrieves product extraction usage metrics from Zyte. |

### Product List Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Product List Extraction Usage](actions/get-product-list-extraction-usage.md) | GET | Retrieves product list extraction usage metrics from Zyte. |

### Product Navigation Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Navigation Extraction Usage](actions/get-product-navigation-extraction-usage.md) | GET | Retrieves product navigation extraction usage metrics from Zyte. |

### Screenshot Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Screenshot Feature Usage](actions/get-screenshot-feature-usage.md) | GET | Retrieves screenshot feature usage metrics from Zyte. |

### Serp Extraction Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get SERP Extraction Usage](actions/get-serp-extraction-usage.md) | GET | Retrieves SERP extraction usage metrics from Zyte. |

### Session Context Feature Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Context Feature Usage](actions/get-session-context-feature-usage.md) | GET | Retrieves session context feature usage metrics from Zyte. |

### Successful Response Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Successful Response Usage](actions/get-successful-response-usage.md) | GET | Retrieves 200 response usage metrics from Zyte. |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Overview](actions/get-usage-overview.md) | GET | Retrieves usage overview metrics from Zyte. |

### Yearly Domain Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Yearly Domain Usage Trend](actions/get-yearly-domain-usage-trend.md) | GET | Retrieves yearly usage trends grouped by domain from Zyte. |

### Yearly Usage Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Yearly Usage Trend](actions/get-yearly-usage-trend.md) | GET | Retrieves yearly usage trends from Zyte. |

