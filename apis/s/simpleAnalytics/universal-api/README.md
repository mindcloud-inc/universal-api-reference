# <img src="https://images.mindcloud.co/apps/icons/simple-analytics_1776178497314.png" alt="Simple Analytics logo" width="28" height="28"> Simple Analytics: Universal API

Simple Analytics provides privacy-friendly website analytics APIs for aggregated stats, raw data exports, and account website administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleAnalytics/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simpleanalytics.com
- **Vendor API docs:** https://docs.simpleanalytics.com/api/authenticate

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Browser Names Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser Names Breakdown](actions/get-browser-names-breakdown.md) | GET | Retrieves a browser breakdown from Simple Analytics. |

### Countries Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Countries Breakdown](actions/get-countries-breakdown.md) | GET | Retrieves a country breakdown from Simple Analytics. |

### Data Point Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Data Points](actions/export-data-points.md) | GET | Exports raw data points from Simple Analytics in JSON. |

### Data Point Export Csv

| Action | Method | Description |
| --- | --- | --- |
| [Export Data Points CSV](actions/export-data-points-csv.md) | GET | Exports raw data points from Simple Analytics in CSV. |

### Device Types Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Types Breakdown](actions/get-device-types-breakdown.md) | GET | Retrieves a device type breakdown from Simple Analytics. |

### Event Counts

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Counts](actions/get-event-counts.md) | GET | Retrieves specified event counts from Simple Analytics. |

### Filtered Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Filtered Stats](actions/get-filtered-stats.md) | GET | Retrieves filtered stats from Simple Analytics. |

### Histogram

| Action | Method | Description |
| --- | --- | --- |
| [Get Histogram](actions/get-histogram.md) | GET | Retrieves histogram stats for a website in Simple Analytics. |

### Hourly Data Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Hourly Data JSON](actions/export-hourly-data-json.md) | GET | Exports hourly data from Simple Analytics in JSON. |

### Hourly Data Export Csv

| Action | Method | Description |
| --- | --- | --- |
| [Export Hourly Data CSV](actions/export-hourly-data-csv.md) | GET | Exports hourly data from Simple Analytics in CSV. |

### Os Names Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get OS Names Breakdown](actions/get-os-names-breakdown.md) | GET | Retrieves an operating system breakdown from Simple Analytics. |

### Page Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Stats](actions/get-page-stats.md) | GET | Retrieves stats for a specific page in Simple Analytics. |

### Pages Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Pages Breakdown](actions/get-pages-breakdown.md) | GET | Retrieves a page breakdown from Simple Analytics. |

### Referrers Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Referrers Breakdown](actions/get-referrers-breakdown.md) | GET | Retrieves a referrer breakdown from Simple Analytics. |

### Seconds On Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Seconds On Page](actions/get-seconds-on-page.md) | GET | Retrieves median seconds on page from Simple Analytics. |

### Utm Campaigns Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Campaigns Breakdown](actions/get-utm-campaigns-breakdown.md) | GET | Retrieves a UTM campaign breakdown from Simple Analytics. |

### Utm Contents Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Contents Breakdown](actions/get-utm-contents-breakdown.md) | GET | Retrieves a UTM content breakdown from Simple Analytics. |

### Utm Mediums Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Mediums Breakdown](actions/get-utm-mediums-breakdown.md) | GET | Retrieves a UTM medium breakdown from Simple Analytics. |

### Utm Sources Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Sources Breakdown](actions/get-utm-sources-breakdown.md) | GET | Retrieves a UTM source breakdown from Simple Analytics. |

### Utm Terms Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Terms Breakdown](actions/get-utm-terms-breakdown.md) | GET | Retrieves a UTM term breakdown from Simple Analytics. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Add Website](actions/add-website.md) | POST | Creates a new website in Simple Analytics. |
| [List Websites](actions/list-websites.md) | GET | Retrieves websites from the authenticated Simple Analytics account. |

### Website Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Stats](actions/get-website-stats.md) | GET | Retrieves aggregated website stats from Simple Analytics. |

