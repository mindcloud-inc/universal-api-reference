# Matomo: Native API Reference

A consolidated summary of Matomo's API configuration and 575 documented operations, with links to official documentation.

- **Official docs:** https://developer.matomo.org/api-reference/reporting-api
- **API base URL:** `https://mindcloud.matomo.cloud`

## Authentication

### Matomo Auth Token

Authenticates Matomo Reporting API calls with a secure auth token sent as token_auth in the POST body.

### Credentials

- **Token Auth:** `tokenAuth` · required · Matomo auth token. For secure-only tokens this is sent as token_auth in the POST body.

[Official authentication documentation](https://developer.matomo.org/api-reference/reporting-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Pagination

Use `filter_limit` in the request body to set the page size (default 100; accepted range 1–1000). Use `filter_offset` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `filter_sort_column` in the request body. Set the direction separately with `filter_sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (575 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [API get Bulk Request](actions/a-pi-get-bulk-request.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Glossary Metrics](actions/a-pi-get-glossary-metrics.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Glossary Reports](actions/a-pi-get-glossary-reports.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Ip From Header](actions/a-pi-get-ip-from-header.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Matomo Version](actions/a-pi-get-matomo-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Metadata](actions/a-pi-get-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Pages Comparisons Disabled For](actions/a-pi-get-pages-comparisons-disabled-for.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Php Version](actions/a-pi-get-php-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Processed Report](actions/a-pi-get-processed-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Report Metadata](actions/a-pi-get-report-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Report Pages Metadata](actions/a-pi-get-report-pages-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Row Evolution](actions/a-pi-get-row-evolution.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Segments Metadata](actions/a-pi-get-segments-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Suggested Values For Segment](actions/a-pi-get-suggested-values-for-segment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API get Widget Metadata](actions/a-pi-get-widget-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [API is Plugin Activated](actions/a-pi-is-plugin-activated.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting add Experiment](actions/ab-testing-add-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting archive Experiment](actions/ab-testing-archive-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting delete Experiment](actions/ab-testing-delete-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting finish Experiment](actions/ab-testing-finish-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Active Experiments](actions/ab-testing-get-active-experiments.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get All Experiments](actions/ab-testing-get-all-experiments.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Available Statuses](actions/ab-testing-get-available-statuses.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Available Success Metrics](actions/ab-testing-get-available-success-metrics.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Available Target Attributes](actions/ab-testing-get-available-target-attributes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Experiment](actions/ab-testing-get-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Experiments By Statuses](actions/ab-testing-get-experiments-by-statuses.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Experiments With Reports](actions/ab-testing-get-experiments-with-reports.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Js Experiment Template](actions/ab-testing-get-js-experiment-template.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Js Include Template](actions/ab-testing-get-js-include-template.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Metric Details](actions/ab-testing-get-metric-details.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting get Metrics Overview](actions/ab-testing-get-metrics-overview.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting start Experiment](actions/ab-testing-start-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AbTesting update Experiment](actions/ab-testing-update-experiment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Actions - Main metrics](actions/actions-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Actions get Download](actions/actions-get-download.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Downloads](actions/actions-get-downloads.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Entry page titles](actions/actions-get-entry-page-titles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Entry pages](actions/actions-get-entry-page-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Exit page titles](actions/actions-get-exit-page-titles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Exit pages](actions/actions-get-exit-page-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Actions get Outlink](actions/actions-get-outlink.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Outlinks](actions/actions-get-outlinks.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Actions get Page Title](actions/actions-get-page-title.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Page titles](actions/actions-get-page-titles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Page Titles Following a Site Search](actions/actions-get-page-titles-following-site-search.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Actions get Page Url](actions/actions-get-page-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Page URLs](actions/actions-get-page-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Pages Following a Site Search](actions/actions-get-page-urls-following-site-search.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Search Categories](actions/actions-get-site-search-categories.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Site Search Keywords](actions/actions-get-site-search-keywords.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Search Keywords with No Results](actions/actions-get-site-search-no-result-keywords.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ActivityLog get All Activity Types](actions/activity-log-get-all-activity-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ActivityLog get Entries](actions/activity-log-get-entries.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ActivityLog get Entry Count](actions/activity-log-get-entry-count.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport add Conversion Export](actions/advertising-conversion-export-add-conversion-export.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport delete Conversion Export](actions/advertising-conversion-export-delete-conversion-export.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport get Conversion Export](actions/advertising-conversion-export-get-conversion-export.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport get Conversion Exports](actions/advertising-conversion-export-get-conversion-exports.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport regenerate Access Token](actions/advertising-conversion-export-regenerate-access-token.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [AdvertisingConversionExport update Conversion Export](actions/advertising-conversion-export-update-conversion-export.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get AI Agent Visits](actions/ai-agents-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations add](actions/annotations-add.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations delete](actions/annotations-delete.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations delete All](actions/annotations-delete-all.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations get](actions/annotations-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations get All](actions/annotations-get-all.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations get Annotation Count For Dates](actions/annotations-get-annotation-count-for-dates.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Annotations save](actions/annotations-save.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Main Metrics](actions/api-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get AI Chatbots Overview](actions/bot-tracking-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get AI Chatbots](actions/bot-tracking-get-ai-chatbot-requests.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [BotTracking get Document Urls For AIChatbot](actions/bot-tracking-get-document-urls-for-ai-chatbot.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [BotTracking get Page Urls For AIChatbot](actions/bot-tracking-get-page-urls-for-ai-chatbot.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ConnectAccounts create Matomo Tag](actions/connect-accounts-create-matomo-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ConnectAccounts get Gtm Containers List](actions/connect-accounts-get-gtm-containers-list.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ConnectAccounts get Gtm Workspace List](actions/connect-accounts-get-gtm-workspace-list.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Content Name](actions/contents-get-content-names.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Content Piece](actions/contents-get-content-pieces.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CoreAdminHome delete All Tracking Failures](actions/core-admin-home-delete-all-tracking-failures.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CoreAdminHome delete Tracking Failure](actions/core-admin-home-delete-tracking-failure.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CoreAdminHome get Tracking Failures](actions/core-admin-home-get-tracking-failures.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get](actions/crash-analytics-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get All Crash Messages](actions/crash-analytics-get-all-crash-messages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get All Crashes](actions/crash-analytics-get-all-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crash Groups](actions/crash-analytics-get-crash-groups.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crash Messages](actions/crash-analytics-get-crash-messages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crash Summary](actions/crash-analytics-get-crash-summary.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crash Types](actions/crash-analytics-get-crash-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crash Visit Context](actions/crash-analytics-get-crash-visit-context.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By Category](actions/crash-analytics-get-crashes-by-category.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By First Party](actions/crash-analytics-get-crashes-by-first-party.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By Page Title](actions/crash-analytics-get-crashes-by-page-title.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By Page Url](actions/crash-analytics-get-crashes-by-page-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By Source](actions/crash-analytics-get-crashes-by-source.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes By Third Party](actions/crash-analytics-get-crashes-by-third-party.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes For Category](actions/crash-analytics-get-crashes-for-category.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes For Page Title](actions/crash-analytics-get-crashes-for-page-title.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes For Page Url](actions/crash-analytics-get-crashes-for-page-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Crashes For Source](actions/crash-analytics-get-crashes-for-source.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Disappeared Crashes](actions/crash-analytics-get-disappeared-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Ignored Crashes](actions/crash-analytics-get-ignored-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Last Crashes Overview](actions/crash-analytics-get-last-crashes-overview.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Last Disappeared Crashes](actions/crash-analytics-get-last-disappeared-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Last New Crashes](actions/crash-analytics-get-last-new-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Last Reappeared Crashes](actions/crash-analytics-get-last-reappeared-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Last Top Crashes](actions/crash-analytics-get-last-top-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get New Crashes](actions/crash-analytics-get-new-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Reappeared Crashes](actions/crash-analytics-get-reappeared-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics get Unidentified Crash Messages](actions/crash-analytics-get-unidentified-crash-messages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics merge Crashes](actions/crash-analytics-merge-crashes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics search Crash Messages For Merge](actions/crash-analytics-search-crash-messages-for-merge.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics set Ignore Crash](actions/crash-analytics-set-ignore-crash.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CrashAnalytics unmerge Crash Group](actions/crash-analytics-unmerge-crash-group.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts add Alert](actions/custom-alerts-add-alert.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts delete Alert](actions/custom-alerts-delete-alert.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts edit Alert](actions/custom-alerts-edit-alert.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts get Alert](actions/custom-alerts-get-alert.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts get Alerts](actions/custom-alerts-get-alerts.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts get Triggered Alerts](actions/custom-alerts-get-triggered-alerts.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomAlerts get Values For Alert In Past](actions/custom-alerts-get-values-for-alert-in-past.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions configure Existing Custom Dimension](actions/custom-dimensions-configure-existing-custom-dimension.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions configure New Custom Dimension](actions/custom-dimensions-configure-new-custom-dimension.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions get Available Extraction Dimensions](actions/custom-dimensions-get-available-extraction-dimensions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions get Available Scopes](actions/custom-dimensions-get-available-scopes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions get Configured Custom Dimensions](actions/custom-dimensions-get-configured-custom-dimensions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions get Configured Custom Dimensions Having Scope](actions/custom-dimensions-get-configured-custom-dimensions-having-scope.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomDimensions get Custom Dimension](actions/custom-dimensions-get-custom-dimension.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomJsTracker does Include Plugin Trackers Automatically](actions/custom-js-tracker-does-include-plugin-trackers-automatically.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports add Custom Report](actions/custom-reports-add-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports delete Custom Report](actions/custom-reports-delete-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports duplicate Custom Report](actions/custom-reports-duplicate-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Available Categories](actions/custom-reports-get-available-categories.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Available Dimensions](actions/custom-reports-get-available-dimensions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Available Metrics](actions/custom-reports-get-available-metrics.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Available Report Types](actions/custom-reports-get-available-report-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Configured Report](actions/custom-reports-get-configured-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Configured Reports](actions/custom-reports-get-configured-reports.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports get Custom Report](actions/custom-reports-get-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports pause Custom Report](actions/custom-reports-pause-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports resume Custom Report](actions/custom-reports-resume-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomReports update Custom Report](actions/custom-reports-update-custom-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomVariables get Custom Variables](actions/custom-variables-get-custom-variables.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomVariables get Custom Variables Values From Name Id](actions/custom-variables-get-custom-variables-values-from-name-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [CustomVariables get Usages Of Slots](actions/custom-variables-get-usages-of-slots.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Dashboard copy Dashboard To User](actions/dashboard-copy-dashboard-to-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Dashboard create New Dashboard For User](actions/dashboard-create-new-dashboard-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Dashboard get Dashboards](actions/dashboard-get-dashboards.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Dashboard remove Dashboard](actions/dashboard-remove-dashboard.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Dashboard reset Dashboard Layout](actions/dashboard-reset-dashboard-layout.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Browser Plugins](actions/device-plugins-get-plugin.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Device brand](actions/devices-detection-get-brand.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Browser engines](actions/devices-detection-get-browser-engines.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Browser version](actions/devices-detection-get-browser-versions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Browsers](actions/devices-detection-get-browsers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Device model](actions/devices-detection-get-model.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Operating System families](actions/devices-detection-get-os-families.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Operating System versions](actions/devices-detection-get-os-versions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Device type](actions/devices-detection-get-type.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Event Actions](actions/events-get-action.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Action From Category Id](actions/events-get-action-from-category-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Action From Name Id](actions/events-get-action-from-name-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Event Categories](actions/events-get-category.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Category From Action Id](actions/events-get-category-from-action-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Category From Name Id](actions/events-get-category-from-name-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Event Names](actions/events-get-name.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Name From Action Id](actions/events-get-name-from-action-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Events get Name From Category Id](actions/events-get-name-from-category-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Feedback send Feedback For Feature](actions/feedback-send-feedback-for-feature.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Feedback send Feedback For Survey](actions/feedback-send-feedback-for-survey.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Feedback update Feedback Reminder Date](actions/feedback-update-feedback-reminder-date.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics add Form](actions/form-analytics-add-form.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics archive Form](actions/form-analytics-archive-form.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics delete Form](actions/form-analytics-delete-form.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Forms Overview](actions/form-analytics-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get All Goals](actions/form-analytics-get-all-goals.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Auto Creation Settings](actions/form-analytics-get-auto-creation-settings.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Available Conversion Rule Options](actions/form-analytics-get-available-conversion-rule-options.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Available Form Rules](actions/form-analytics-get-available-form-rules.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Available Page Rules](actions/form-analytics-get-available-page-rules.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Available Statuses](actions/form-analytics-get-available-statuses.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Counters](actions/form-analytics-get-counters.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Current Most Popular Forms](actions/form-analytics-get-current-most-popular-forms.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Drop Off Fields](actions/form-analytics-get-drop-off-fields.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Entry Fields](actions/form-analytics-get-entry-fields.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Field Corrections](actions/form-analytics-get-field-corrections.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Field Size](actions/form-analytics-get-field-size.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Field Timings](actions/form-analytics-get-field-timings.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Form](actions/form-analytics-get-form.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Forms](actions/form-analytics-get-forms.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Forms By Statuses](actions/form-analytics-get-forms-by-statuses.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Most Used Fields](actions/form-analytics-get-most-used-fields.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Page Urls](actions/form-analytics-get-page-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics get Uneeded Fields](actions/form-analytics-get-uneeded-fields.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics update Form](actions/form-analytics-update-form.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [FormAnalytics update Form Field Display Name](actions/form-analytics-update-form-field-display-name.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels delete Goal Funnel](actions/funnels-delete-goal-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels delete Non Goal Funnel](actions/funnels-delete-non-goal-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get All Activated Funnels For Site](actions/funnels-get-all-activated-funnels-for-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Available Pattern Matches](actions/funnels-get-available-pattern-matches.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel](actions/funnels-get-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel Entries](actions/funnels-get-funnel-entries.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel Exits](actions/funnels-get-funnel-exits.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel Flow](actions/funnels-get-funnel-flow.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel Flow Table](actions/funnels-get-funnel-flow-table.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Funnel Step Subtable](actions/funnels-get-funnel-step-subtable.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Goal Funnel](actions/funnels-get-goal-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Metrics](actions/funnels-get-metrics.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels get Sales Funnel For Site](actions/funnels-get-sales-funnel-for-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels has Any Activated Funnel For Site](actions/funnels-has-any-activated-funnel-for-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels save Non Goal Funnel](actions/funnels-save-non-goal-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels set Goal Funnel](actions/funnels-set-goal-funnel.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Funnels test Url Matches Steps](actions/funnels-test-url-matches-steps.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Matomo Version](actions/get-matomo-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Goals add Goal](actions/goals-add-goal.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Goals delete Goal](actions/goals-delete-goal.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Ecommerce Orders](actions/goals-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Ecommerce Orders - Days to Conversion](actions/goals-get-days-to-conversion.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Goals get Goal](actions/goals-get-goal.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Goals get Goals](actions/goals-get-goals.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Product Category](actions/goals-get-items-category.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Product Name](actions/goals-get-items-name.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Product SKU](actions/goals-get-items-sku.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Ecommerce Orders - Visits to Conversion](actions/goals-get-visits-until-conversion.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Goals update Goal](actions/goals-update-goal.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording add Heatmap](actions/heatmap-session-recording-add-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording add Session Recording](actions/heatmap-session-recording-add-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording delete Heatmap](actions/heatmap-session-recording-delete-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording delete Heatmap Screenshot](actions/heatmap-session-recording-delete-heatmap-screenshot.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording delete Recorded Pageview](actions/heatmap-session-recording-delete-recorded-pageview.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording delete Recorded Session](actions/heatmap-session-recording-delete-recorded-session.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording delete Session Recording](actions/heatmap-session-recording-delete-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording duplicate Heatmap](actions/heatmap-session-recording-duplicate-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording end Heatmap](actions/heatmap-session-recording-end-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording end Session Recording](actions/heatmap-session-recording-end-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Available Device Types](actions/heatmap-session-recording-get-available-device-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Available Heatmap Types](actions/heatmap-session-recording-get-available-heatmap-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Available Session Recording Sample Limits](actions/heatmap-session-recording-get-available-session-recording-sample-limits.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Available Statuses](actions/heatmap-session-recording-get-available-statuses.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Available Target Page Rules](actions/heatmap-session-recording-get-available-target-page-rules.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Embed Session Info](actions/heatmap-session-recording-get-embed-session-info.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Event Types](actions/heatmap-session-recording-get-event-types.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Heatmap](actions/heatmap-session-recording-get-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Heatmaps](actions/heatmap-session-recording-get-heatmaps.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Recorded Heatmap](actions/heatmap-session-recording-get-recorded-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Recorded Heatmap Metadata](actions/heatmap-session-recording-get-recorded-heatmap-metadata.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Recorded Session](actions/heatmap-session-recording-get-recorded-session.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Recorded Sessions](actions/heatmap-session-recording-get-recorded-sessions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Session Recording](actions/heatmap-session-recording-get-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording get Session Recordings](actions/heatmap-session-recording-get-session-recordings.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording pause Heatmap](actions/heatmap-session-recording-pause-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording pause Session Recording](actions/heatmap-session-recording-pause-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording resume Heatmap](actions/heatmap-session-recording-resume-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording resume Session Recording](actions/heatmap-session-recording-resume-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording test Url Match Pages](actions/heatmap-session-recording-test-url-match-pages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording update Heatmap](actions/heatmap-session-recording-update-heatmap.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [HeatmapSessionRecording update Session Recording](actions/heatmap-session-recording-update-session-recording.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ImageGraph get](actions/image-graph-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Insights can Generate Insights](actions/insights-can-generate-insights.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Insights get Insights](actions/insights-get-insights.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Insights get Insights Overview](actions/insights-get-insights-overview.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Insights get Movers And Shakers](actions/insights-get-movers-and-shakers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Insights get Movers And Shakers Overview](actions/insights-get-movers-and-shakers-overview.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager get Available Language Names](actions/languages-manager-get-available-language-names.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager get Available Languages](actions/languages-manager-get-available-languages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager get Available Languages Info](actions/languages-manager-get-available-languages-info.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager get Language For User](actions/languages-manager-get-language-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager get Translations For Language](actions/languages-manager-get-translations-for-language.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager is Language Available](actions/languages-manager-is-language-available.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager set Language For User](actions/languages-manager-set-language-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager set12 Hour Clock For User](actions/languages-manager-set12-hour-clock-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [LanguagesManager uses12 Hour Clock For User](actions/languages-manager-uses12-hour-clock-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live get Counters](actions/live-get-counters.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live get Last Visits Details](actions/live-get-last-visits-details.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live get Most Recent Visitor Id](actions/live-get-most-recent-visitor-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live get Most Recent Visits Date Time](actions/live-get-most-recent-visits-date-time.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live get Visitor Profile](actions/live-get-visitor-profile.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Live is Visitor Profile Enabled](actions/live-is-visitor-profile-enabled.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Login unblock Brute Force IPs](actions/login-unblock-brute-force-i-ps.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Contents](actions/marketing-campaigns-reporting-get-content.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Groups](actions/marketing-campaigns-reporting-get-group.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Ids](actions/marketing-campaigns-reporting-get-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Keywords](actions/marketing-campaigns-reporting-get-keyword.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MarketingCampaignsReporting get Keyword Content From Name Id](actions/marketing-campaigns-reporting-get-keyword-content-from-name-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Mediums](actions/marketing-campaigns-reporting-get-medium.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Names](actions/marketing-campaigns-reporting-get-name.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MarketingCampaignsReporting get Name From Source Medium Id](actions/marketing-campaigns-reporting-get-name-from-source-medium-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Placements](actions/marketing-campaigns-reporting-get-placement.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Sources](actions/marketing-campaigns-reporting-get-source.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Campaign Source - Medium](actions/marketing-campaigns-reporting-get-source-medium.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Media Summary](actions/media-analytics-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Audio per hour in website timezone](actions/media-analytics-get-audio-hours.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Audio Resource URLs](actions/media-analytics-get-audio-resources.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Audio Titles](actions/media-analytics-get-audio-titles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MediaAnalytics get Current Most Plays](actions/media-analytics-get-current-most-plays.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MediaAnalytics get Current Num Plays](actions/media-analytics-get-current-num-plays.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MediaAnalytics get Current Sum Time Spent](actions/media-analytics-get-current-sum-time-spent.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Audio Resources URLs Grouped](actions/media-analytics-get-grouped-audio-resources.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Video Resource URLs Grouped](actions/media-analytics-get-grouped-video-resources.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Media Players](actions/media-analytics-get-players.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Videos per hour in website's timezone](actions/media-analytics-get-video-hours.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Video Resolutions](actions/media-analytics-get-video-resolutions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Video Resource URLs](actions/media-analytics-get-video-resources.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Video Titles](actions/media-analytics-get-video-titles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MediaAnalytics has Records](actions/media-analytics-has-records.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging add Phone Number](actions/mobile-messaging-add-phone-number.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging are SMSAPICredential Provided](actions/mobile-messaging-are-smsapi-credential-provided.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging delete SMSAPICredential](actions/mobile-messaging-delete-smsapi-credential.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging get Credit Left](actions/mobile-messaging-get-credit-left.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging get Delegated Management](actions/mobile-messaging-get-delegated-management.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging get Phone Numbers](actions/mobile-messaging-get-phone-numbers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging get SMSProvider](actions/mobile-messaging-get-sms-provider.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging remove Phone Number](actions/mobile-messaging-remove-phone-number.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging resend Verification Code](actions/mobile-messaging-resend-verification-code.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging set Delegated Management](actions/mobile-messaging-set-delegated-management.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging set SMSAPICredential](actions/mobile-messaging-set-smsapi-credential.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MobileMessaging validate Phone Number](actions/mobile-messaging-validate-phone-number.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiChannelConversionAttribution get Available Campaign Dimension Combinations](actions/multi-channel-conversion-attribution-get-available-campaign-dimension-combinations.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiChannelConversionAttribution get Channel Attribution](actions/multi-channel-conversion-attribution-get-channel-attribution.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiChannelConversionAttribution get Goal Attribution](actions/multi-channel-conversion-attribution-get-goal-attribution.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiChannelConversionAttribution get Site Attribution Goals](actions/multi-channel-conversion-attribution-get-site-attribution-goals.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiChannelConversionAttribution set Goal Attribution](actions/multi-channel-conversion-attribution-set-goal-attribution.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get All Websites dashboard](actions/multi-sites-get-all.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [MultiSites get All With Groups](actions/multi-sites-get-all-with-groups.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Single Website dashboard](actions/multi-sites-get-one.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 create Client](actions/o-auth2-create-client.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 delete Client](actions/o-auth2-delete-client.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 get Client](actions/o-auth2-get-client.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 get Clients](actions/o-auth2-get-clients.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 get Scopes](actions/o-auth2-get-scopes.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 rotate Secret](actions/o-auth2-rotate-secret.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 set Client Active](actions/o-auth2-set-client-active.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OAuth2 update Client](actions/o-auth2-update-client.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OpenApiDocs get Generated Open Api Spec](actions/open-api-docs-get-generated-open-api-spec.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OpenApiDocs get Open Api Spec](actions/open-api-docs-get-open-api-spec.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [OpenApiDocs get Plugin Whitelist](actions/open-api-docs-get-plugin-whitelist.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Overlay get Following Pages](actions/overlay-get-following-pages.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Overlay get Translations](actions/overlay-get-translations.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Performance overview](actions/page-performance-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager anonymize Some Raw Data](actions/privacy-manager-anonymize-some-raw-data.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager delete Data Subjects](actions/privacy-manager-delete-data-subjects.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager export Data Subjects](actions/privacy-manager-export-data-subjects.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager find Data Subjects](actions/privacy-manager-find-data-subjects.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager get Available Link Visit Action Columns To Anonymize](actions/privacy-manager-get-available-link-visit-action-columns-to-anonymize.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [PrivacyManager get Available Visit Columns To Anonymize](actions/privacy-manager-get-available-visit-columns-to-anonymize.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Referrers Overview](actions/referrers-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get AI Assistants](actions/referrers-get-ai-assistants.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get All Channels](actions/referrers-get-all.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Campaigns](actions/referrers-get-campaigns.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Entry Page Titles For AIAssistant](actions/referrers-get-entry-page-titles-for-ai-assistant.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Entry Page Urls For AIAssistant](actions/referrers-get-entry-page-urls-for-ai-assistant.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Keywords](actions/referrers-get-keywords.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Keywords From Campaign Id](actions/referrers-get-keywords-from-campaign-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Keywords From Search Engine Id](actions/referrers-get-keywords-from-search-engine-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct AIAssistants](actions/referrers-get-number-of-distinct-ai-assistants.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Campaigns](actions/referrers-get-number-of-distinct-campaigns.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Keywords](actions/referrers-get-number-of-distinct-keywords.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Search Engines](actions/referrers-get-number-of-distinct-search-engines.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Social Networks](actions/referrers-get-number-of-distinct-social-networks.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Websites](actions/referrers-get-number-of-distinct-websites.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Number Of Distinct Websites Urls](actions/referrers-get-number-of-distinct-websites-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Channel Type](actions/referrers-get-referrer-type.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Search Engines](actions/referrers-get-search-engines.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Search Engines From Keyword Id](actions/referrers-get-search-engines-from-keyword-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Social Networks](actions/referrers-get-socials.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Urls For Social](actions/referrers-get-urls-for-social.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Referrers get Urls From Website Id](actions/referrers-get-urls-from-website-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Websites](actions/referrers-get-websites.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Configurations](actions/resolution-get-configuration.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Screen Resolution](actions/resolution-get-resolution.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [RollUpReporting add Roll Up](actions/roll-up-reporting-add-roll-up.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [RollUpReporting get Roll Ups](actions/roll-up-reporting-get-roll-ups.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [RollUpReporting update Roll Up](actions/roll-up-reporting-update-roll-up.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SEO get Rank](actions/s-eo-get-rank.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports add Report](actions/scheduled-reports-add-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports delete Report](actions/scheduled-reports-delete-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports generate Report](actions/scheduled-reports-generate-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports get Reports](actions/scheduled-reports-get-reports.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports send Report](actions/scheduled-reports-send-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [ScheduledReports update Report](actions/scheduled-reports-update-report.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Crawling Error Examples Bing](actions/search-engine-keywords-performance-get-crawling-error-examples-bing.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Crawling Overview Bing](actions/search-engine-keywords-performance-get-crawling-overview-bing.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Crawling Overview Yandex](actions/search-engine-keywords-performance-get-crawling-overview-yandex.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords](actions/search-engine-keywords-performance-get-keywords.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Bing](actions/search-engine-keywords-performance-get-keywords-bing.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Google](actions/search-engine-keywords-performance-get-keywords-google.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Google Image](actions/search-engine-keywords-performance-get-keywords-google-image.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Google News](actions/search-engine-keywords-performance-get-keywords-google-news.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Google Video](actions/search-engine-keywords-performance-get-keywords-google-video.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Google Web](actions/search-engine-keywords-performance-get-keywords-google-web.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Imported](actions/search-engine-keywords-performance-get-keywords-imported.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SearchEngineKeywordsPerformance get Keywords Yandex](actions/search-engine-keywords-performance-get-keywords-yandex.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor add](actions/segment-editor-add.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor delete](actions/segment-editor-delete.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor get](actions/segment-editor-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor get All](actions/segment-editor-get-all.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor get Segment Data](actions/segment-editor-get-segment-data.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor is User Can Add New Segment](actions/segment-editor-is-user-can-add-new-segment.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor star](actions/segment-editor-star.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor unstar](actions/segment-editor-unstar.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SegmentEditor update](actions/segment-editor-update.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager add Site](actions/sites-manager-add-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager add Site Alias Urls](actions/sites-manager-add-site-alias-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager delete Site](actions/sites-manager-delete-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get All Sites](actions/sites-manager-get-all-sites.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get All Sites Id](actions/sites-manager-get-all-sites-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Currency List](actions/sites-manager-get-currency-list.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Currency Symbols](actions/sites-manager-get-currency-symbols.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Default Currency](actions/sites-manager-get-default-currency.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Default Timezone](actions/sites-manager-get-default-timezone.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded Ips Global](actions/sites-manager-get-excluded-ips-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded Query Parameters](actions/sites-manager-get-excluded-query-parameters.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded Query Parameters Global](actions/sites-manager-get-excluded-query-parameters-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded Referrers](actions/sites-manager-get-excluded-referrers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded Referrers Global](actions/sites-manager-get-excluded-referrers-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Excluded User Agents Global](actions/sites-manager-get-excluded-user-agents-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Exclusion Type For Query Params](actions/sites-manager-get-exclusion-type-for-query-params.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Image Tracking Code](actions/sites-manager-get-image-tracking-code.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Ips For Range](actions/sites-manager-get-ips-for-range.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Javascript Tag](actions/sites-manager-get-javascript-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Keep URLFragments Global](actions/sites-manager-get-keep-url-fragments-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Num Websites To Display Per Page](actions/sites-manager-get-num-websites-to-display-per-page.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Pattern Match Sites](actions/sites-manager-get-pattern-match-sites.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Search Category Parameters Global](actions/sites-manager-get-search-category-parameters-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Search Keyword Parameters Global](actions/sites-manager-get-search-keyword-parameters-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Site From Id](actions/sites-manager-get-site-from-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Site Settings](actions/sites-manager-get-site-settings.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Site Urls From Id](actions/sites-manager-get-site-urls-from-id.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites From Group](actions/sites-manager-get-sites-from-group.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Groups](actions/sites-manager-get-sites-groups.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Id From Site Url](actions/sites-manager-get-sites-id-from-site-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Id With Admin Access](actions/sites-manager-get-sites-id-with-admin-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Id With At Least View Access](actions/sites-manager-get-sites-id-with-at-least-view-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Id With View Access](actions/sites-manager-get-sites-id-with-view-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites Id With Write Access](actions/sites-manager-get-sites-id-with-write-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites With Admin Access](actions/sites-manager-get-sites-with-admin-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites With At Least View Access](actions/sites-manager-get-sites-with-at-least-view-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites With Minimum Access](actions/sites-manager-get-sites-with-minimum-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Sites With View Access](actions/sites-manager-get-sites-with-view-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Timezone Name](actions/sites-manager-get-timezone-name.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Timezones List](actions/sites-manager-get-timezones-list.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager get Unique Site Timezones](actions/sites-manager-get-unique-site-timezones.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager is Timezone Support Enabled](actions/sites-manager-is-timezone-support-enabled.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager rename Group](actions/sites-manager-rename-group.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Default Currency](actions/sites-manager-set-default-currency.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Default Timezone](actions/sites-manager-set-default-timezone.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Global Excluded Ips](actions/sites-manager-set-global-excluded-ips.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Global Excluded Referrers](actions/sites-manager-set-global-excluded-referrers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Global Excluded User Agents](actions/sites-manager-set-global-excluded-user-agents.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Global Query Param Exclusion](actions/sites-manager-set-global-query-param-exclusion.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Global Search Parameters](actions/sites-manager-set-global-search-parameters.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Keep URLFragments Global](actions/sites-manager-set-keep-url-fragments-global.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager set Site Alias Urls](actions/sites-manager-set-site-alias-urls.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [SitesManager update Site](actions/sites-manager-update-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager add Container](actions/tag-manager-add-container.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager add Container Tag](actions/tag-manager-add-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager add Container Trigger](actions/tag-manager-add-container-trigger.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager add Container Variable](actions/tag-manager-add-container-variable.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager change Debug Url](actions/tag-manager-change-debug-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager create Container Version](actions/tag-manager-create-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager create Default Container For Site](actions/tag-manager-create-default-container-for-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager delete Container](actions/tag-manager-delete-container.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager delete Container Tag](actions/tag-manager-delete-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager delete Container Trigger](actions/tag-manager-delete-container-trigger.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager delete Container Variable](actions/tag-manager-delete-container-variable.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager delete Container Version](actions/tag-manager-delete-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager disable Preview Mode](actions/tag-manager-disable-preview-mode.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager enable Preview Mode](actions/tag-manager-enable-preview-mode.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager export Container Version](actions/tag-manager-export-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Comparisons](actions/tag-manager-get-available-comparisons.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Container Variables](actions/tag-manager-get-available-container-variables.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Contexts](actions/tag-manager-get-available-contexts.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Environments](actions/tag-manager-get-available-environments.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Environments With Publish Capability](actions/tag-manager-get-available-environments-with-publish-capability.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Tag Fire Limits](actions/tag-manager-get-available-tag-fire-limits.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Tag Types In Context](actions/tag-manager-get-available-tag-types-in-context.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Trigger Types In Context](actions/tag-manager-get-available-trigger-types-in-context.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Available Variable Types In Context](actions/tag-manager-get-available-variable-types-in-context.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container](actions/tag-manager-get-container.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Embed Code](actions/tag-manager-get-container-embed-code.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Install Instructions](actions/tag-manager-get-container-install-instructions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Tag](actions/tag-manager-get-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Tags](actions/tag-manager-get-container-tags.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Trigger](actions/tag-manager-get-container-trigger.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Trigger References](actions/tag-manager-get-container-trigger-references.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Triggers](actions/tag-manager-get-container-triggers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Variable](actions/tag-manager-get-container-variable.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Variable References](actions/tag-manager-get-container-variable-references.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Variables](actions/tag-manager-get-container-variables.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Version](actions/tag-manager-get-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Container Versions](actions/tag-manager-get-container-versions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager get Containers](actions/tag-manager-get-containers.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager import Container Version](actions/tag-manager-import-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager pause Container Tag](actions/tag-manager-pause-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager publish Container Version](actions/tag-manager-publish-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager resume Container Tag](actions/tag-manager-resume-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager update Container](actions/tag-manager-update-container.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager update Container Tag](actions/tag-manager-update-container-tag.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager update Container Trigger](actions/tag-manager-update-container-trigger.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager update Container Variable](actions/tag-manager-update-container-variable.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TagManager update Container Version](actions/tag-manager-update-container-version.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Tour get Challenges](actions/tour-get-challenges.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Tour get Level](actions/tour-get-level.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Tour skip Challenge](actions/tour-skip-challenge.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Transitions get Transitions For Action](actions/transitions-get-transitions-for-action.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Transitions get Transitions For Page Title](actions/transitions-get-transitions-for-page-title.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Transitions get Transitions For Page Url](actions/transitions-get-transitions-for-page-url.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Transitions get Translations](actions/transitions-get-translations.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Transitions is Period Allowed](actions/transitions-is-period-allowed.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [TwoFactorAuth reset Two Factor Auth](actions/two-factor-auth-reset-two-factor-auth.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get City](actions/user-country-get-city.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Continent](actions/user-country-get-continent.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Country](actions/user-country-get-country.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UserCountry get Country Code Mapping](actions/user-country-get-country-code-mapping.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UserCountry get Location From IP](actions/user-country-get-location-from-ip.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UserCountry get Number Of Distinct Countries](actions/user-country-get-number-of-distinct-countries.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Region](actions/user-country-get-region.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UserCountry set Location Provider](actions/user-country-set-location-provider.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get User IDs](actions/user-id-get-users.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Web-browser language](actions/user-language-get-language.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Language code](actions/user-language-get-language-code.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersFlow get Available Data Sources](actions/users-flow-get-available-data-sources.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersFlow get Interaction Actions](actions/users-flow-get-interaction-actions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersFlow get Users Flow](actions/users-flow-get-users-flow.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Users Flow](actions/users-flow-get-users-flow-pretty.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager add Capabilities](actions/users-manager-add-capabilities.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager add User](actions/users-manager-add-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager create App Specific Token Auth](actions/users-manager-create-app-specific-token-auth.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager delete User](actions/users-manager-delete-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager generate Invite Link](actions/users-manager-generate-invite-link.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Available Capabilities](actions/users-manager-get-available-capabilities.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Available Roles](actions/users-manager-get-available-roles.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Sites Access For User](actions/users-manager-get-sites-access-for-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Sites Access From User](actions/users-manager-get-sites-access-from-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get User](actions/users-manager-get-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get User By Email](actions/users-manager-get-user-by-email.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get User Login From User Email](actions/users-manager-get-user-login-from-user-email.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get User Preference](actions/users-manager-get-user-preference.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users](actions/users-manager-get-users.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users Access From Site](actions/users-manager-get-users-access-from-site.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users Having Super User Access](actions/users-manager-get-users-having-super-user-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users Login](actions/users-manager-get-users-login.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users Plus Role](actions/users-manager-get-users-plus-role.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users Sites From Access](actions/users-manager-get-users-sites-from-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager get Users With Site Access](actions/users-manager-get-users-with-site-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager has Super User Access](actions/users-manager-has-super-user-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager invite User](actions/users-manager-invite-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager logout User](actions/users-manager-logout-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager newsletter Signup](actions/users-manager-newsletter-signup.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager remove Capabilities](actions/users-manager-remove-capabilities.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager resend Invite](actions/users-manager-resend-invite.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager set Super User Access](actions/users-manager-set-super-user-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager set User Access](actions/users-manager-set-user-access.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager set User Preference](actions/users-manager-set-user-preference.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager update User](actions/users-manager-update-user.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager user Email Exists](actions/users-manager-user-email-exists.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [UsersManager user Exists](actions/users-manager-user-exists.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Returning Visits](actions/visit-frequency-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits by day of the week](actions/visit-time-get-by-day-of-week.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits per local time](actions/visit-time-get-visit-information-per-local-time.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits per hour in the site's timezone](actions/visit-time-get-visit-information-per-server-time.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits by days since last visit](actions/visitor-interest-get-number-of-visits-by-days-since-last.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits by visit number](actions/visitor-interest-get-number-of-visits-by-visit-count.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Pages per visit](actions/visitor-interest-get-number-of-visits-per-page.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Length of visits](actions/visitor-interest-get-number-of-visits-per-visit-duration.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Get Visits Summary](actions/visits-summary-get.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Actions](actions/visits-summary-get-actions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Bounce Count](actions/visits-summary-get-bounce-count.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Max Actions](actions/visits-summary-get-max-actions.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Sum Visits Length](actions/visits-summary-get-sum-visits-length.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Sum Visits Length Pretty](actions/visits-summary-get-sum-visits-length-pretty.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Unique Visitors](actions/visits-summary-get-unique-visitors.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Users](actions/visits-summary-get-users.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Visits](actions/visits-summary-get-visits.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
| [VisitsSummary get Visits Converted](actions/visits-summary-get-visits-converted.md) | `POST /index.php` | [docs](https://developer.matomo.org/api-reference/reporting-api) |
