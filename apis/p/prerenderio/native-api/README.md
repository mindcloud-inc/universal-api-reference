# Prerender.io: Native API Reference

A consolidated summary of Prerender.io's API configuration and 90 documented operations, with links to official documentation.

- **Official docs:** https://docs.prerender.io/docs/6-api
- **OpenAPI specification:** https://api.prerender.io/v3/api-json
- **API base URL:** `https://api.prerender.io`

## Authentication

### API Token

Use a Prerender API token from Security and Access. The runtime sends it in the x-prerender-api-key header.

### Credentials

- **API Token:** `apiToken` · required · Prerender API token used for the x-prerender-api-key header.

Send these headers with each API request:

```http
x-prerender-api-key: <apiToken>
```

[Official authentication documentation](https://docs.prerender.io/docs/6-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (90 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Domain 404 Check](actions/delete-v3-domain-404-check-id.md) | `DELETE /v3/domain-404-check/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Delete Domain Keyword Rankings](actions/delete-v3-domain-keyword-rankings-id.md) | `DELETE /v3/domain-keyword-rankings/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Delete Gsc Integrations](actions/delete-v3-gsc-integrations.md) | `DELETE /v3/gsc-integrations` | [docs](https://api.prerender.io/v3/api) |
| [Delete Render Queue Manual](actions/delete-v3-render-queue-manual.md) | `DELETE /v3/render-queue/manual` | [docs](https://api.prerender.io/v3/api) |
| [Delete Sitemap](actions/delete-v3-sitemap-id.md) | `DELETE /v3/sitemap/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Delete Urls Cache](actions/delete-v3-urls-cache.md) | `DELETE /v3/urls/cache` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Delivered Daily](actions/get-v3-aggregated-metrics-page-delivered-daily.md) | `GET /v3/aggregated-metrics/page-delivered/daily` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Delivered Status Code Daily](actions/get-v3-aggregated-metrics-page-delivered-status-code-daily.md) | `GET /v3/aggregated-metrics/page-delivered-status-code/daily` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Delivered Status Code Overview](actions/get-v3-aggregated-metrics-page-delivered-status-code-overview.md) | `GET /v3/aggregated-metrics/page-delivered-status-code/overview` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Delivered User Agent Daily](actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily.md) | `GET /v3/aggregated-metrics/page-delivered-user-agent/daily` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Delivered User Agent Overview](actions/get-v3-aggregated-metrics-page-delivered-user-agent-overview.md) | `GET /v3/aggregated-metrics/page-delivered-user-agent/overview` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Rendered Status Code Daily](actions/get-v3-aggregated-metrics-page-rendered-status-code-daily.md) | `GET /v3/aggregated-metrics/page-rendered-status-code/daily` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Page Rendered Status Code Overview](actions/get-v3-aggregated-metrics-page-rendered-status-code-overview.md) | `GET /v3/aggregated-metrics/page-rendered-status-code/overview` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Renders Daily](actions/get-v3-aggregated-metrics-renders-daily.md) | `GET /v3/aggregated-metrics/renders/daily` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Trial Overview](actions/get-v3-aggregated-metrics-trial-overview.md) | `GET /v3/aggregated-metrics/trial-overview` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Usage Overview](actions/get-v3-aggregated-metrics-usage-overview.md) | `GET /v3/aggregated-metrics/usage-overview` | [docs](https://api.prerender.io/v3/api) |
| [List Ai Insights Diagnostics](actions/get-v3-ai-insights-diagnostics.md) | `GET /v3/ai-insights/diagnostics` | [docs](https://api.prerender.io/v3/api) |
| [Get Ai Insights Diagnostics](actions/get-v3-ai-insights-diagnostics-reportid.md) | `GET /v3/ai-insights/diagnostics/{reportId}` | [docs](https://api.prerender.io/v3/api) |
| [List Analytics Crawled Pages](actions/get-v3-analytics-crawled-pages.md) | `GET /v3/analytics/crawled-pages` | [docs](https://api.prerender.io/v3/api) |
| [List Billing Estimation](actions/get-v3-billing-estimation.md) | `GET /v3/billing/estimation` | [docs](https://api.prerender.io/v3/api) |
| [List Billing Expense Monthly](actions/get-v3-billing-expense-monthly.md) | `GET /v3/billing/expense/monthly` | [docs](https://api.prerender.io/v3/api) |
| [List Billing Invoices](actions/get-v3-billing-invoices.md) | `GET /v3/billing/invoices` | [docs](https://api.prerender.io/v3/api) |
| [Get Billing Invoices Download Link](actions/get-v3-billing-invoices-id-download-link.md) | `GET /v3/billing/invoices/{id}/download-link` | [docs](https://api.prerender.io/v3/api) |
| [List Billing Is Payment Info Valid](actions/get-v3-billing-is-payment-info-valid.md) | `GET /v3/billing/is-payment-info-valid` | [docs](https://api.prerender.io/v3/api) |
| [List Coupons](actions/get-v3-coupons.md) | `GET /v3/coupons` | [docs](https://api.prerender.io/v3/api) |
| [List Domain 404 Check](actions/get-v3-domain-404-check.md) | `GET /v3/domain-404-check` | [docs](https://api.prerender.io/v3/api) |
| [List Domain Keyword Rankings](actions/get-v3-domain-keyword-rankings.md) | `GET /v3/domain-keyword-rankings` | [docs](https://api.prerender.io/v3/api) |
| [Get Domain Keyword Rankings](actions/get-v3-domain-keyword-rankings-id.md) | `GET /v3/domain-keyword-rankings/{id}` | [docs](https://api.prerender.io/v3/api) |
| [List Domains](actions/get-v3-domains.md) | `GET /v3/domains` | [docs](https://api.prerender.io/v3/api) |
| [List Domains Company Config](actions/get-v3-domains-company-config.md) | `GET /v3/domains/company/config` | [docs](https://api.prerender.io/v3/api) |
| [Get Domains Config](actions/get-v3-domains-domain-config.md) | `GET /v3/domains/{domain}/config` | [docs](https://api.prerender.io/v3/api) |
| [Get Domains Last Cached Urls](actions/get-v3-domains-domain-last-cached-urls.md) | `GET /v3/domains/{domain}/last-cached-urls` | [docs](https://api.prerender.io/v3/api) |
| [List Environment](actions/get-v3-environment.md) | `GET /v3/environment` | [docs](https://api.prerender.io/v3/api) |
| [List Events History](actions/get-v3-events-history.md) | `GET /v3/events-history` | [docs](https://api.prerender.io/v3/api) |
| [List Gsc Integrations Sitemaps](actions/get-v3-gsc-integrations-sitemaps.md) | `GET /v3/gsc-integrations/sitemaps` | [docs](https://api.prerender.io/v3/api) |
| [List Gsc Integrations Sites](actions/get-v3-gsc-integrations-sites.md) | `GET /v3/gsc-integrations/sites` | [docs](https://api.prerender.io/v3/api) |
| [List Gsc Integrations Status](actions/get-v3-gsc-integrations-status.md) | `GET /v3/gsc-integrations/status` | [docs](https://api.prerender.io/v3/api) |
| [List Notifications](actions/get-v3-notifications.md) | `GET /v3/notifications` | [docs](https://api.prerender.io/v3/api) |
| [Get Notifications](actions/get-v3-notifications-id.md) | `GET /v3/notifications/{id}` | [docs](https://api.prerender.io/v3/api) |
| [List Referrals](actions/get-v3-referrals.md) | `GET /v3/referrals` | [docs](https://api.prerender.io/v3/api) |
| [List Referrals Stats](actions/get-v3-referrals-stats.md) | `GET /v3/referrals/stats` | [docs](https://api.prerender.io/v3/api) |
| [List Renders Report](actions/get-v3-renders-report.md) | `GET /v3/renders/report` | [docs](https://api.prerender.io/v3/api) |
| [List Seo Score Details](actions/get-v3-seo-score-details.md) | `GET /v3/seo/score/details` | [docs](https://api.prerender.io/v3/api) |
| [List Seo Score Summary](actions/get-v3-seo-score-summary.md) | `GET /v3/seo/score/summary` | [docs](https://api.prerender.io/v3/api) |
| [List Seo Urls](actions/get-v3-seo-urls.md) | `GET /v3/seo/urls` | [docs](https://api.prerender.io/v3/api) |
| [List Sitemap](actions/get-v3-sitemap.md) | `GET /v3/sitemap` | [docs](https://api.prerender.io/v3/api) |
| [Get Sitemap](actions/get-v3-sitemap-id.md) | `GET /v3/sitemap/{id}` | [docs](https://api.prerender.io/v3/api) |
| [List Ui State](actions/get-v3-ui-state.md) | `GET /v3/ui-state` | [docs](https://api.prerender.io/v3/api) |
| [List Urls](actions/get-v3-urls.md) | `GET /v3/urls` | [docs](https://api.prerender.io/v3/api) |
| [List Urls Cache Clear Status](actions/get-v3-urls-cache-clear-status.md) | `GET /v3/urls/cache-clear-status` | [docs](https://api.prerender.io/v3/api) |
| [List Urls Count](actions/get-v3-urls-count.md) | `GET /v3/urls/count` | [docs](https://api.prerender.io/v3/api) |
| [List Urls Report](actions/get-v3-urls-report.md) | `GET /v3/urls/report` | [docs](https://api.prerender.io/v3/api) |
| [List User Event Log](actions/get-v3-user-event-log.md) | `GET /v3/user-event-log` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Cache Hit Miss Time](actions/get-v4-aggregated-metrics-cache-hit-miss-time.md) | `GET /v4/aggregated-metrics/cache-hit-miss-time` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Cache Hits Ratio Summary](actions/get-v4-aggregated-metrics-cache-hits-ratio-summary.md) | `GET /v4/aggregated-metrics/cache-hits-ratio-summary` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Crawlers](actions/get-v4-aggregated-metrics-crawlers.md) | `GET /v4/aggregated-metrics/crawlers` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Delivery Times](actions/get-v4-aggregated-metrics-delivery-times.md) | `GET /v4/aggregated-metrics/delivery-times` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Delivery Times Summary](actions/get-v4-aggregated-metrics-delivery-times-summary.md) | `GET /v4/aggregated-metrics/delivery-times-summary` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Error Rate Summary](actions/get-v4-aggregated-metrics-error-rate-summary.md) | `GET /v4/aggregated-metrics/error-rate-summary` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Pages Crawled](actions/get-v4-aggregated-metrics-pages-crawled.md) | `GET /v4/aggregated-metrics/pages-crawled` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Pages Crawled Summary](actions/get-v4-aggregated-metrics-pages-crawled-summary.md) | `GET /v4/aggregated-metrics/pages-crawled-summary` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Pages Crawled Volume](actions/get-v4-aggregated-metrics-pages-crawled-volume.md) | `GET /v4/aggregated-metrics/pages-crawled-volume` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Pages Rendered](actions/get-v4-aggregated-metrics-pages-rendered.md) | `GET /v4/aggregated-metrics/pages-rendered` | [docs](https://api.prerender.io/v3/api) |
| [List Aggregated Metrics Status Codes](actions/get-v4-aggregated-metrics-status-codes.md) | `GET /v4/aggregated-metrics/status-codes` | [docs](https://api.prerender.io/v3/api) |
| [Update Domain 404 Check Toggle All](actions/patch-v3-domain-404-check-toggle-all-enabled.md) | `PATCH /v3/domain-404-check/toggle-all/{enabled}` | [docs](https://api.prerender.io/v3/api) |
| [Update Domains Config](actions/patch-v3-domains-domain-config.md) | `PATCH /v3/domains/{domain}/config` | [docs](https://api.prerender.io/v3/api) |
| [Update Environment](actions/patch-v3-environment.md) | `PATCH /v3/environment` | [docs](https://api.prerender.io/v3/api) |
| [Update Notifications Mark As Seen](actions/patch-v3-notifications-mark-as-seen.md) | `PATCH /v3/notifications/mark-as-seen` | [docs](https://api.prerender.io/v3/api) |
| [Update Sitemap](actions/patch-v3-sitemap-id.md) | `PATCH /v3/sitemap/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Update Sitemap Toggle All](actions/patch-v3-sitemap-toggle-all-enabled.md) | `PATCH /v3/sitemap/toggle-all/{enabled}` | [docs](https://api.prerender.io/v3/api) |
| [Create Ai Insights Diagnostics](actions/post-v3-ai-insights-diagnostics.md) | `POST /v3/ai-insights/diagnostics` | [docs](https://api.prerender.io/v3/api) |
| [Create Analytics Crawled Pages Export](actions/post-v3-analytics-crawled-pages-export.md) | `POST /v3/analytics/crawled-pages/export` | [docs](https://api.prerender.io/v3/api) |
| [Create Cdn Analytics Export](actions/post-v3-cdn-analytics-export.md) | `POST /v3/cdn-analytics-export` | [docs](https://api.prerender.io/v3/api) |
| [Create Cdn Requests Per Domain Export](actions/post-v3-cdn-requests-per-domain-export.md) | `POST /v3/cdn-requests-per-domain-export` | [docs](https://api.prerender.io/v3/api) |
| [Create Coupons Apply](actions/post-v3-coupons-apply-id.md) | `POST /v3/coupons/apply/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Create Coupons Deactivate](actions/post-v3-coupons-deactivate-id.md) | `POST /v3/coupons/deactivate/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Create Domain 404 Check](actions/post-v3-domain-404-check.md) | `POST /v3/domain-404-check` | [docs](https://api.prerender.io/v3/api) |
| [Create Domain 404 Check Bulk](actions/post-v3-domain-404-check-bulk.md) | `POST /v3/domain-404-check/bulk` | [docs](https://api.prerender.io/v3/api) |
| [Create Domain Keyword Rankings](actions/post-v3-domain-keyword-rankings.md) | `POST /v3/domain-keyword-rankings` | [docs](https://api.prerender.io/v3/api) |
| [Create Gsc Integrations](actions/post-v3-gsc-integrations.md) | `POST /v3/gsc-integrations` | [docs](https://api.prerender.io/v3/api) |
| [Create Gsc Integrations Sitemaps Imports](actions/post-v3-gsc-integrations-sitemaps-imports.md) | `POST /v3/gsc-integrations/sitemaps/imports` | [docs](https://api.prerender.io/v3/api) |
| [Create Referrals](actions/post-v3-referrals.md) | `POST /v3/referrals` | [docs](https://api.prerender.io/v3/api) |
| [Create Sitemap](actions/post-v3-sitemap.md) | `POST /v3/sitemap` | [docs](https://api.prerender.io/v3/api) |
| [Create Sitemap Crawl](actions/post-v3-sitemap-id-crawl.md) | `POST /v3/sitemap/{id}/crawl` | [docs](https://api.prerender.io/v3/api) |
| [Create Tawkto Sign](actions/post-v3-tawkto-sign.md) | `POST /v3/tawkto/sign` | [docs](https://api.prerender.io/v3/api) |
| [Create Ui State](actions/post-v3-ui-state-type.md) | `POST /v3/ui-state/{type}` | [docs](https://api.prerender.io/v3/api) |
| [Create Urls](actions/post-v3-urls.md) | `POST /v3/urls` | [docs](https://api.prerender.io/v3/api) |
| [Create Userflow Sign](actions/post-v3-userflow-sign.md) | `POST /v3/userflow/sign` | [docs](https://api.prerender.io/v3/api) |
| [Update Domain 404 Check](actions/put-v3-domain-404-check-id.md) | `PUT /v3/domain-404-check/{id}` | [docs](https://api.prerender.io/v3/api) |
| [Update Domain Keyword Rankings](actions/put-v3-domain-keyword-rankings-id.md) | `PUT /v3/domain-keyword-rankings/{id}` | [docs](https://api.prerender.io/v3/api) |
