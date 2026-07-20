# <img src="https://images.mindcloud.co/apps/icons/prerender-icon_1776184107078.png" alt="Prerender.io logo" width="28" height="28"> Prerender.io: Universal API

Prerender.io is a search-engine rendering and cache-management platform for JavaScript-heavy websites, with APIs for environment settings, cached URLs, sitemaps, domains, SEO metrics, analytics, notifications, and related account operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prerenderio/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 90
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://prerender.io
- **Vendor API docs:** https://docs.prerender.io/docs/6-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Environment](actions/get-v3-environment.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-environment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (90)

### Aggregated Metrics Cache Hit Miss Time

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Cache Hit Miss Time](actions/get-v4-aggregated-metrics-cache-hit-miss-time.md) | GET | Retrieves cache hit-miss time metrics from Prerender.io. |

### Aggregated Metrics Cache Hits Ratio Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Cache Hits Ratio Summary](actions/get-v4-aggregated-metrics-cache-hits-ratio-summary.md) | GET | Retrieves a cache hits ratio summary from Prerender.io. |

### Aggregated Metrics Crawlers

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Crawlers](actions/get-v4-aggregated-metrics-crawlers.md) | GET | Retrieves crawler metrics from Prerender.io. |

### Aggregated Metrics Delivery Times

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Delivery Times](actions/get-v4-aggregated-metrics-delivery-times.md) | GET | Retrieves delivery time metrics from Prerender.io. |

### Aggregated Metrics Delivery Times Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Delivery Times Summary](actions/get-v4-aggregated-metrics-delivery-times-summary.md) | GET | Retrieves a delivery times summary from Prerender.io. |

### Aggregated Metrics Error Rate Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Error Rate Summary](actions/get-v4-aggregated-metrics-error-rate-summary.md) | GET | Retrieves an error rate summary from Prerender.io. |

### Aggregated Metrics Page Delivered Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Delivered Daily](actions/get-v3-aggregated-metrics-page-delivered-daily.md) | GET | Retrieves daily delivered page metrics from Prerender.io. |

### Aggregated Metrics Page Delivered Status Code Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Delivered Status Code Daily](actions/get-v3-aggregated-metrics-page-delivered-status-code-daily.md) | GET | Retrieves daily delivered page status code metrics from Prerender.io. |

### Aggregated Metrics Page Delivered Status Code Overview

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Delivered Status Code Overview](actions/get-v3-aggregated-metrics-page-delivered-status-code-overview.md) | GET | Retrieves an overview of delivered page status code metrics from Prerender.io. |

### Aggregated Metrics Page Delivered User Agent Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Delivered User Agent Daily](actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily.md) | GET | Retrieves daily delivered page user agent metrics from Prerender.io. |

### Aggregated Metrics Page Delivered User Agent Overview

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Delivered User Agent Overview](actions/get-v3-aggregated-metrics-page-delivered-user-agent-overview.md) | GET | Retrieves an overview of delivered page user agent metrics from Prerender.io. |

### Aggregated Metrics Page Rendered Status Code Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Rendered Status Code Daily](actions/get-v3-aggregated-metrics-page-rendered-status-code-daily.md) | GET | Retrieves daily rendered page status code metrics from Prerender.io. |

### Aggregated Metrics Page Rendered Status Code Overview

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Page Rendered Status Code Overview](actions/get-v3-aggregated-metrics-page-rendered-status-code-overview.md) | GET | Retrieves an overview of rendered page status code metrics from Prerender.io. |

### Aggregated Metrics Pages Crawled

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Pages Crawled](actions/get-v4-aggregated-metrics-pages-crawled.md) | GET | Retrieves pages crawled metrics from Prerender.io. |

### Aggregated Metrics Pages Crawled Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Pages Crawled Summary](actions/get-v4-aggregated-metrics-pages-crawled-summary.md) | GET | Retrieves a pages crawled summary from Prerender.io. |

### Aggregated Metrics Pages Crawled Volume

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Pages Crawled Volume](actions/get-v4-aggregated-metrics-pages-crawled-volume.md) | GET | Retrieves pages crawled volume metrics from Prerender.io. |

### Aggregated Metrics Pages Rendered

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Pages Rendered](actions/get-v4-aggregated-metrics-pages-rendered.md) | GET | Retrieves pages rendered metrics from Prerender.io. |

### Aggregated Metrics Renders Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Renders Daily](actions/get-v3-aggregated-metrics-renders-daily.md) | GET | Retrieves daily render metrics from Prerender.io. |

### Aggregated Metrics Status Codes

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Status Codes](actions/get-v4-aggregated-metrics-status-codes.md) | GET | Retrieves status code metrics from Prerender.io. |

### Aggregated Metrics Trial Overview

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Trial Overview](actions/get-v3-aggregated-metrics-trial-overview.md) | GET | Retrieves a trial overview from Prerender.io. |

### Aggregated Metrics Usage Overview

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Metrics Usage Overview](actions/get-v3-aggregated-metrics-usage-overview.md) | GET | Retrieves a usage overview from Prerender.io. |

### Ai Insights Diagnostics

| Action | Method | Description |
| --- | --- | --- |
| [List Ai Insights Diagnostics](actions/get-v3-ai-insights-diagnostics.md) | GET | Retrieves AI insights diagnostics from Prerender.io. |
| [Get Ai Insights Diagnostics](actions/get-v3-ai-insights-diagnostics-reportid.md) | GET | Retrieves an AI insights diagnostics report from Prerender.io. |
| [Create Ai Insights Diagnostics](actions/post-v3-ai-insights-diagnostics.md) | POST | Creates an AI insights diagnostics report in Prerender.io. |

### Analytics Crawled Pages

| Action | Method | Description |
| --- | --- | --- |
| [List Analytics Crawled Pages](actions/get-v3-analytics-crawled-pages.md) | GET | Retrieves analytics crawled pages from Prerender.io. |

### Analytics Crawled Pages Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Analytics Crawled Pages Export](actions/post-v3-analytics-crawled-pages-export.md) | POST | Creates an analytics crawled pages export in Prerender.io. |

### Billing Estimation

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Estimation](actions/get-v3-billing-estimation.md) | GET | Retrieves billing estimation from Prerender.io. |

### Billing Expense Monthly

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Expense Monthly](actions/get-v3-billing-expense-monthly.md) | GET | Retrieves monthly billing expenses from Prerender.io. |

### Billing Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Invoices](actions/get-v3-billing-invoices.md) | GET | Retrieves billing invoices from Prerender.io. |

### Billing Invoices Download Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Invoices Download Link](actions/get-v3-billing-invoices-id-download-link.md) | GET | Retrieves an invoice download link from Prerender.io. |

### Billing Is Payment Info Valid

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Is Payment Info Valid](actions/get-v3-billing-is-payment-info-valid.md) | GET | Retrieves payment info validation from Prerender.io. |

### Cdn Analytics Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Cdn Analytics Export](actions/post-v3-cdn-analytics-export.md) | POST | Creates a CDN analytics export in Prerender.io. |

### Cdn Requests Per Domain Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Cdn Requests Per Domain Export](actions/post-v3-cdn-requests-per-domain-export.md) | POST | Creates a CDN requests-per-domain export in Prerender.io. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [List Coupons](actions/get-v3-coupons.md) | GET | Retrieves coupons from Prerender.io. |

### Coupons Apply

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupons Apply](actions/post-v3-coupons-apply-id.md) | POST | Applies a coupon in Prerender.io. |

### Coupons Deactivate

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupons Deactivate](actions/post-v3-coupons-deactivate-id.md) | POST | Deactivates a coupon in Prerender.io. |

### Domain 404 Check

| Action | Method | Description |
| --- | --- | --- |
| [Delete Domain 404 Check](actions/delete-v3-domain-404-check-id.md) | DELETE | Deletes a domain 404 check from Prerender.io. |
| [List Domain 404 Check](actions/get-v3-domain-404-check.md) | GET | Retrieves domain 404 checks from Prerender.io. |
| [Create Domain 404 Check](actions/post-v3-domain-404-check.md) | POST | Creates a domain 404 check in Prerender.io. |
| [Update Domain 404 Check](actions/put-v3-domain-404-check-id.md) | PUT | Updates a domain 404 check in Prerender.io. |

### Domain 404 Check Bulk

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain 404 Check Bulk](actions/post-v3-domain-404-check-bulk.md) | POST | Creates bulk domain 404 checks in Prerender.io. |

### Domain 404 Check Toggle All

| Action | Method | Description |
| --- | --- | --- |
| [Update Domain 404 Check Toggle All](actions/patch-v3-domain-404-check-toggle-all-enabled.md) | PUT | Updates all domain 404 checks in Prerender.io. |

### Domain Keyword Rankings

| Action | Method | Description |
| --- | --- | --- |
| [Delete Domain Keyword Rankings](actions/delete-v3-domain-keyword-rankings-id.md) | DELETE | Deletes a domain keyword ranking from Prerender.io. |
| [List Domain Keyword Rankings](actions/get-v3-domain-keyword-rankings.md) | GET | Retrieves domain keyword rankings from Prerender.io. |
| [Get Domain Keyword Rankings](actions/get-v3-domain-keyword-rankings-id.md) | GET | Retrieves a domain keyword ranking from Prerender.io. |
| [Create Domain Keyword Rankings](actions/post-v3-domain-keyword-rankings.md) | POST | Creates a domain keyword ranking in Prerender.io. |
| [Update Domain Keyword Rankings](actions/put-v3-domain-keyword-rankings-id.md) | PUT | Updates a domain keyword ranking in Prerender.io. |

### Domains

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/get-v3-domains.md) | GET | Retrieves domains from Prerender.io. |

### Domains Company Config

| Action | Method | Description |
| --- | --- | --- |
| [List Domains Company Config](actions/get-v3-domains-company-config.md) | GET | Retrieves company domain config from Prerender.io. |

### Domains Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Domains Config](actions/get-v3-domains-domain-config.md) | GET | Retrieves config for a domain from Prerender.io. |
| [Update Domains Config](actions/patch-v3-domains-domain-config.md) | PUT | Updates config for a domain in Prerender.io. |

### Domains Last Cached Urls

| Action | Method | Description |
| --- | --- | --- |
| [Get Domains Last Cached Urls](actions/get-v3-domains-domain-last-cached-urls.md) | GET | Retrieves a domain's last cached URLs from Prerender.io. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [List Environment](actions/get-v3-environment.md) | GET | Retrieves environment settings from Prerender.io. |
| [Update Environment](actions/patch-v3-environment.md) | PUT | Updates environment settings in Prerender.io. |

### Events History

| Action | Method | Description |
| --- | --- | --- |
| [List Events History](actions/get-v3-events-history.md) | GET | Retrieves event history from Prerender.io. |

### Gsc Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Delete Gsc Integrations](actions/delete-v3-gsc-integrations.md) | DELETE | Deletes the GSC integration from Prerender.io. |
| [Create Gsc Integrations](actions/post-v3-gsc-integrations.md) | POST | Creates a GSC integration in Prerender.io. |

### Gsc Integrations Sitemaps

| Action | Method | Description |
| --- | --- | --- |
| [List Gsc Integrations Sitemaps](actions/get-v3-gsc-integrations-sitemaps.md) | GET | Retrieves GSC integration sitemaps from Prerender.io. |

### Gsc Integrations Sitemaps Imports

| Action | Method | Description |
| --- | --- | --- |
| [Create Gsc Integrations Sitemaps Imports](actions/post-v3-gsc-integrations-sitemaps-imports.md) | POST | Creates a GSC sitemap import in Prerender.io. |

### Gsc Integrations Sites

| Action | Method | Description |
| --- | --- | --- |
| [List Gsc Integrations Sites](actions/get-v3-gsc-integrations-sites.md) | GET | Retrieves GSC integration sites from Prerender.io. |

### Gsc Integrations Status

| Action | Method | Description |
| --- | --- | --- |
| [List Gsc Integrations Status](actions/get-v3-gsc-integrations-status.md) | GET | Retrieves GSC integration status from Prerender.io. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/get-v3-notifications.md) | GET | Retrieves notifications from Prerender.io. |
| [Get Notifications](actions/get-v3-notifications-id.md) | GET | Retrieves a notification from Prerender.io. |

### Notifications Mark As Seen

| Action | Method | Description |
| --- | --- | --- |
| [Update Notifications Mark As Seen](actions/patch-v3-notifications-mark-as-seen.md) | PUT | Updates notifications as seen in Prerender.io. |

### Referrals

| Action | Method | Description |
| --- | --- | --- |
| [List Referrals](actions/get-v3-referrals.md) | GET | Retrieves referrals from Prerender.io. |
| [Create Referrals](actions/post-v3-referrals.md) | POST | Creates a referral in Prerender.io. |

### Referrals Stats

| Action | Method | Description |
| --- | --- | --- |
| [List Referrals Stats](actions/get-v3-referrals-stats.md) | GET | Retrieves referral stats from Prerender.io. |

### Render Queue Manual

| Action | Method | Description |
| --- | --- | --- |
| [Delete Render Queue Manual](actions/delete-v3-render-queue-manual.md) | DELETE | Deletes manual render queue entries from Prerender.io. |

### Renders Report

| Action | Method | Description |
| --- | --- | --- |
| [List Renders Report](actions/get-v3-renders-report.md) | GET | Retrieves a renders report from Prerender.io. |

### Seo Score Details

| Action | Method | Description |
| --- | --- | --- |
| [List Seo Score Details](actions/get-v3-seo-score-details.md) | GET | Retrieves SEO score details from Prerender.io. |

### Seo Score Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Seo Score Summary](actions/get-v3-seo-score-summary.md) | GET | Retrieves an SEO score summary from Prerender.io. |

### Seo Urls

| Action | Method | Description |
| --- | --- | --- |
| [List Seo Urls](actions/get-v3-seo-urls.md) | GET | Retrieves SEO URLs from Prerender.io. |

### Sitemap

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sitemap](actions/delete-v3-sitemap-id.md) | DELETE | Deletes a sitemap entry from Prerender.io. |
| [List Sitemap](actions/get-v3-sitemap.md) | GET | Retrieves sitemap entries from Prerender.io. |
| [Get Sitemap](actions/get-v3-sitemap-id.md) | GET | Retrieves a sitemap entry from Prerender.io. |
| [Update Sitemap](actions/patch-v3-sitemap-id.md) | PUT | Updates a sitemap entry in Prerender.io. |
| [Create Sitemap](actions/post-v3-sitemap.md) | POST | Creates a sitemap entry in Prerender.io. |

### Sitemap Crawl

| Action | Method | Description |
| --- | --- | --- |
| [Create Sitemap Crawl](actions/post-v3-sitemap-id-crawl.md) | POST | Starts a sitemap crawl in Prerender.io. |

### Sitemap Toggle All

| Action | Method | Description |
| --- | --- | --- |
| [Update Sitemap Toggle All](actions/patch-v3-sitemap-toggle-all-enabled.md) | PUT | Updates all sitemap entries in Prerender.io. |

### Tawkto Sign

| Action | Method | Description |
| --- | --- | --- |
| [Create Tawkto Sign](actions/post-v3-tawkto-sign.md) | POST | Creates a Tawk.to signature in Prerender.io. |

### Ui State

| Action | Method | Description |
| --- | --- | --- |
| [List Ui State](actions/get-v3-ui-state.md) | GET | Retrieves UI state from Prerender.io. |
| [Create Ui State](actions/post-v3-ui-state-type.md) | POST | Creates a UI state entry in Prerender.io. |

### Urls

| Action | Method | Description |
| --- | --- | --- |
| [List Urls](actions/get-v3-urls.md) | GET | Retrieves URLs from Prerender.io. |
| [Create Urls](actions/post-v3-urls.md) | POST | Creates a URL in Prerender.io. |

### Urls Cache

| Action | Method | Description |
| --- | --- | --- |
| [Delete Urls Cache](actions/delete-v3-urls-cache.md) | DELETE | Deletes cached URLs from Prerender.io. |

### Urls Cache Clear Status

| Action | Method | Description |
| --- | --- | --- |
| [List Urls Cache Clear Status](actions/get-v3-urls-cache-clear-status.md) | GET | Retrieves URL cache clear status from Prerender.io. |

### Urls Count

| Action | Method | Description |
| --- | --- | --- |
| [List Urls Count](actions/get-v3-urls-count.md) | GET | Retrieves a URL count from Prerender.io. |

### Urls Report

| Action | Method | Description |
| --- | --- | --- |
| [List Urls Report](actions/get-v3-urls-report.md) | GET | Retrieves a URLs report from Prerender.io. |

### User Event Log

| Action | Method | Description |
| --- | --- | --- |
| [List User Event Log](actions/get-v3-user-event-log.md) | GET | Retrieves the user event log from Prerender.io. |

### Userflow Sign

| Action | Method | Description |
| --- | --- | --- |
| [Create Userflow Sign](actions/post-v3-userflow-sign.md) | POST | Creates a Userflow signature in Prerender.io. |

