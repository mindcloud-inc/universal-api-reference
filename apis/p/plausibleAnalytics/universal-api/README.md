# <img src="https://images.mindcloud.co/apps/icons/plausible-analytics_1776954176426.png" alt="Plausible Analytics logo" width="28" height="28"> Plausible Analytics: Universal API

Plausible Analytics is a privacy-friendly web analytics platform for querying traffic metrics, managing sites, and sending events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plausibleAnalytics/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://plausible.io
- **Vendor API docs:** https://plausible.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Api Health

| Action | Method | Description |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | GET | Retrieves Plausible Analytics API health status. |

### Behavioral Filter Result

| Action | Method | Description |
| --- | --- | --- |
| [Apply Behavioral Filters](actions/apply-behavioral-filters.md) | GET | Retrieves stats from Plausible Analytics using behavioral filters. |

### Browser Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser Breakdown](actions/get-browser-breakdown.md) | GET | Retrieves browser breakdown metrics from Plausible Analytics. |

### Campaign Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Breakdown](actions/get-campaign-breakdown.md) | GET | Retrieves campaign breakdown metrics from Plausible Analytics. |

### Case Insensitive Filter Result

| Action | Method | Description |
| --- | --- | --- |
| [Filter Case Insensitively](actions/filter-case-insensitively.md) | GET | Retrieves filtered stats from Plausible Analytics using case-insensitive matching. |

### Channel Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Breakdown](actions/get-channel-breakdown.md) | GET | Retrieves channel breakdown metrics from Plausible Analytics. |

### City Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get City Breakdown](actions/get-city-breakdown.md) | GET | Retrieves city breakdown metrics from Plausible Analytics. |

### Country And City Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Country and City Analysis](actions/get-country-and-city-analysis.md) | GET | Retrieves country and city metrics from Plausible Analytics. |

### Custom Date Range Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Date Range Stats](actions/get-custom-date-range-stats.md) | GET | Retrieves custom date range stats from Plausible Analytics. |

### Custom Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Property](actions/create-custom-property.md) | POST | Creates a custom property in a Plausible Analytics site. |
| [Delete Custom Property](actions/delete-custom-property.md) | DELETE | Deletes a custom property from a Plausible Analytics site. |
| [List Custom Properties](actions/list-custom-properties.md) | GET | Retrieves custom properties from a Plausible Analytics site. |

### Custom Property Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Query by Custom Properties](actions/query-by-custom-properties.md) | GET | Retrieves stats from Plausible Analytics using custom properties. |

### Custom Property Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Property Breakdown](actions/get-custom-property-breakdown.md) | GET | Retrieves custom property breakdown metrics from Plausible Analytics. |

### Device Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Breakdown](actions/get-device-breakdown.md) | GET | Retrieves device breakdown metrics from Plausible Analytics. |

### Entry Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Entry Pages](actions/get-entry-pages.md) | GET | Retrieves entry pages from Plausible Analytics. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Event](actions/send-event.md) | POST | Sends a pageview or custom event to Plausible Analytics. |

### Exit Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Exit Pages](actions/get-exit-pages.md) | GET | Retrieves exit pages from Plausible Analytics. |

### Filtered Stats

| Action | Method | Description |
| --- | --- | --- |
| [Filter by Page and Country](actions/filter-by-page-and-country.md) | GET | Retrieves stats from Plausible Analytics filtered by page and country. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Delete Goal](actions/delete-goal.md) | DELETE | Deletes an existing goal from a Plausible Analytics site. |
| [List Goals](actions/list-goals.md) | GET | Retrieves goals from a Plausible Analytics site. |
| [Upsert Goal](actions/upsert-goal.md) | PUT | Finds or creates a goal in a Plausible Analytics site. |

### Goal Conversion Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Goal Conversions](actions/get-goal-conversions.md) | GET | Retrieves goal conversion metrics from Plausible Analytics. |

### Guest

| Action | Method | Description |
| --- | --- | --- |
| [List Guests](actions/list-guests.md) | GET | Retrieves guest invitations and memberships from a Plausible Analytics site. |

### Guest Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Guest](actions/delete-guest.md) | DELETE | Deletes a guest invitation or membership from a Plausible Analytics site. |
| [Invite Guest](actions/invite-guest.md) | POST | Creates a guest invitation in a Plausible Analytics site. |

### Hourly Time Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Hourly Time Labels](actions/get-hourly-time-labels.md) | GET | Retrieves hourly time-series metrics with labels from Plausible Analytics. |

### Imported Data Report

| Action | Method | Description |
| --- | --- | --- |
| [Include Imported Data](actions/include-imported-data.md) | GET | Retrieves stats from Plausible Analytics including imported data. |

### Landing Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Landing Pages](actions/get-landing-pages.md) | GET | Retrieves landing pages from Plausible Analytics. |

### Operating System Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Operating System Breakdown](actions/get-operating-system-breakdown.md) | GET | Retrieves operating system breakdown metrics from Plausible Analytics. |

### Paginated Stats Result

| Action | Method | Description |
| --- | --- | --- |
| [Paginate Stats Results](actions/paginate-stats-results.md) | GET | Retrieves paginated stats results from Plausible Analytics. |

### Realtime Visitors

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime Visitors](actions/get-realtime-visitors.md) | GET | Retrieves real-time visitor counts from Plausible Analytics. |

### Referrer Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Referrer Breakdown](actions/get-referrer-breakdown.md) | GET | Retrieves referrer breakdown metrics from Plausible Analytics. |

### Region Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Region Breakdown](actions/get-region-breakdown.md) | GET | Retrieves region breakdown metrics from Plausible Analytics. |

### Revenue Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Revenue Metrics](actions/get-revenue-metrics.md) | GET | Retrieves revenue metrics from Plausible Analytics. |

### Segment Filter Result

| Action | Method | Description |
| --- | --- | --- |
| [Filter by Segment](actions/filter-by-segment.md) | GET | Retrieves segment-filtered stats from Plausible Analytics. |

### Shared Link

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Shared Link](actions/upsert-shared-link.md) | PUT | Finds or creates a shared dashboard link in Plausible Analytics. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Plausible Analytics. |
| [Delete Site](actions/delete-site.md) | DELETE | Deletes an existing site from Plausible Analytics. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Plausible Analytics by domain. |
| [List Sites](actions/list-sites.md) | GET | Retrieves accessible sites from Plausible Analytics. |
| [Update Site](actions/update-site.md) | PUT | Updates an existing site in Plausible Analytics. |

### Stats Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Stats](actions/query-stats.md) | GET | Retrieves historical or real-time stats from Plausible Analytics. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves accessible teams from Plausible Analytics. |

### Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Series](actions/get-time-series.md) | GET | Retrieves time-series metrics from Plausible Analytics. |

### Top Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Countries](actions/get-top-countries.md) | GET | Retrieves top countries from Plausible Analytics. |

### Top Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Pages](actions/get-top-pages.md) | GET | Retrieves top pages from Plausible Analytics. |

### Top Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Sources](actions/get-top-sources.md) | GET | Retrieves top traffic sources from Plausible Analytics. |

### Traffic Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Traffic Summary](actions/get-traffic-summary.md) | GET | Retrieves traffic summary metrics from Plausible Analytics. |

### Utm Source Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Source Analysis](actions/get-utm-source-analysis.md) | GET | Retrieves UTM source and medium metrics from Plausible Analytics. |

