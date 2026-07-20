# <img src="https://images.mindcloud.co/apps/icons/matomo-icon-square_1776787654476.png" alt="Matomo logo" width="28" height="28"> Matomo: Universal API

Matomo analytics and administration API for querying visitor, acquisition, content, event, goal, ecommerce, and site configuration data from a Matomo Cloud instance.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/matomo/latest
- **Actions:** 575
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://matomo.org/
- **Vendor API docs:** https://developer.matomo.org/api-reference/reporting-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Matomo Version](actions/get-matomo-version.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-matomo-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (575)

### Abtesting

| Action | Method | Description |
| --- | --- | --- |
| [AbTesting add Experiment](actions/ab-testing-add-experiment.md) | POST |  |
| [AbTesting archive Experiment](actions/ab-testing-archive-experiment.md) | DELETE |  |
| [AbTesting delete Experiment](actions/ab-testing-delete-experiment.md) | DELETE |  |
| [AbTesting finish Experiment](actions/ab-testing-finish-experiment.md) | PUT |  |
| [AbTesting get Active Experiments](actions/ab-testing-get-active-experiments.md) | GET |  |
| [AbTesting get All Experiments](actions/ab-testing-get-all-experiments.md) | GET |  |
| [AbTesting get Available Statuses](actions/ab-testing-get-available-statuses.md) | GET |  |
| [AbTesting get Available Success Metrics](actions/ab-testing-get-available-success-metrics.md) | GET |  |
| [AbTesting get Available Target Attributes](actions/ab-testing-get-available-target-attributes.md) | GET |  |
| [AbTesting get Experiment](actions/ab-testing-get-experiment.md) | GET |  |
| [AbTesting get Experiments By Statuses](actions/ab-testing-get-experiments-by-statuses.md) | GET |  |
| [AbTesting get Experiments With Reports](actions/ab-testing-get-experiments-with-reports.md) | GET |  |
| [AbTesting get Js Experiment Template](actions/ab-testing-get-js-experiment-template.md) | GET |  |
| [AbTesting get Js Include Template](actions/ab-testing-get-js-include-template.md) | GET |  |
| [AbTesting get Metric Details](actions/ab-testing-get-metric-details.md) | GET |  |
| [AbTesting get Metrics Overview](actions/ab-testing-get-metrics-overview.md) | GET |  |
| [AbTesting start Experiment](actions/ab-testing-start-experiment.md) | PUT |  |
| [AbTesting update Experiment](actions/ab-testing-update-experiment.md) | PUT |  |

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Actions get Download](actions/actions-get-download.md) | GET |  |
| [Actions get Outlink](actions/actions-get-outlink.md) | GET |  |
| [Actions get Page Title](actions/actions-get-page-title.md) | GET |  |
| [Actions get Page Url](actions/actions-get-page-url.md) | GET |  |

### Activitylog

| Action | Method | Description |
| --- | --- | --- |
| [ActivityLog get All Activity Types](actions/activity-log-get-all-activity-types.md) | GET |  |
| [ActivityLog get Entries](actions/activity-log-get-entries.md) | GET |  |
| [ActivityLog get Entry Count](actions/activity-log-get-entry-count.md) | GET |  |

### Advertisingconversionexport

| Action | Method | Description |
| --- | --- | --- |
| [AdvertisingConversionExport add Conversion Export](actions/advertising-conversion-export-add-conversion-export.md) | POST |  |
| [AdvertisingConversionExport delete Conversion Export](actions/advertising-conversion-export-delete-conversion-export.md) | DELETE |  |
| [AdvertisingConversionExport get Conversion Export](actions/advertising-conversion-export-get-conversion-export.md) | GET |  |
| [AdvertisingConversionExport get Conversion Exports](actions/advertising-conversion-export-get-conversion-exports.md) | GET |  |
| [AdvertisingConversionExport regenerate Access Token](actions/advertising-conversion-export-regenerate-access-token.md) | GET |  |
| [AdvertisingConversionExport update Conversion Export](actions/advertising-conversion-export-update-conversion-export.md) | PUT |  |

### Annotations

| Action | Method | Description |
| --- | --- | --- |
| [Annotations add](actions/annotations-add.md) | POST |  |
| [Annotations delete](actions/annotations-delete.md) | DELETE |  |
| [Annotations delete All](actions/annotations-delete-all.md) | DELETE |  |
| [Annotations get](actions/annotations-get.md) | GET |  |
| [Annotations get All](actions/annotations-get-all.md) | GET |  |
| [Annotations get Annotation Count For Dates](actions/annotations-get-annotation-count-for-dates.md) | GET |  |
| [Annotations save](actions/annotations-save.md) | GET |  |

### Api

| Action | Method | Description |
| --- | --- | --- |
| [API get Bulk Request](actions/a-pi-get-bulk-request.md) | GET |  |
| [API get Glossary Metrics](actions/a-pi-get-glossary-metrics.md) | GET |  |
| [API get Glossary Reports](actions/a-pi-get-glossary-reports.md) | GET |  |
| [API get Ip From Header](actions/a-pi-get-ip-from-header.md) | GET |  |
| [API get Matomo Version](actions/a-pi-get-matomo-version.md) | GET |  |
| [API get Metadata](actions/a-pi-get-metadata.md) | GET |  |
| [API get Pages Comparisons Disabled For](actions/a-pi-get-pages-comparisons-disabled-for.md) | GET |  |
| [API get Php Version](actions/a-pi-get-php-version.md) | GET |  |
| [API get Processed Report](actions/a-pi-get-processed-report.md) | GET |  |
| [API get Report Metadata](actions/a-pi-get-report-metadata.md) | GET |  |
| [API get Report Pages Metadata](actions/a-pi-get-report-pages-metadata.md) | GET |  |
| [API get Row Evolution](actions/a-pi-get-row-evolution.md) | GET |  |
| [API get Segments Metadata](actions/a-pi-get-segments-metadata.md) | GET |  |
| [API get Suggested Values For Segment](actions/a-pi-get-suggested-values-for-segment.md) | GET |  |
| [API get Widget Metadata](actions/a-pi-get-widget-metadata.md) | GET |  |
| [API is Plugin Activated](actions/a-pi-is-plugin-activated.md) | GET |  |

### Bottracking

| Action | Method | Description |
| --- | --- | --- |
| [BotTracking get Document Urls For AIChatbot](actions/bot-tracking-get-document-urls-for-ai-chatbot.md) | GET |  |
| [BotTracking get Page Urls For AIChatbot](actions/bot-tracking-get-page-urls-for-ai-chatbot.md) | GET |  |

### Connectaccounts

| Action | Method | Description |
| --- | --- | --- |
| [ConnectAccounts create Matomo Tag](actions/connect-accounts-create-matomo-tag.md) | POST |  |
| [ConnectAccounts get Gtm Containers List](actions/connect-accounts-get-gtm-containers-list.md) | GET |  |
| [ConnectAccounts get Gtm Workspace List](actions/connect-accounts-get-gtm-workspace-list.md) | GET |  |

### Coreadminhome

| Action | Method | Description |
| --- | --- | --- |
| [CoreAdminHome delete All Tracking Failures](actions/core-admin-home-delete-all-tracking-failures.md) | DELETE |  |
| [CoreAdminHome delete Tracking Failure](actions/core-admin-home-delete-tracking-failure.md) | DELETE |  |
| [CoreAdminHome get Tracking Failures](actions/core-admin-home-get-tracking-failures.md) | GET |  |

### Crashanalytics

| Action | Method | Description |
| --- | --- | --- |
| [CrashAnalytics get](actions/crash-analytics-get.md) | GET |  |
| [CrashAnalytics get All Crash Messages](actions/crash-analytics-get-all-crash-messages.md) | GET |  |
| [CrashAnalytics get All Crashes](actions/crash-analytics-get-all-crashes.md) | GET |  |
| [CrashAnalytics get Crash Groups](actions/crash-analytics-get-crash-groups.md) | GET |  |
| [CrashAnalytics get Crash Messages](actions/crash-analytics-get-crash-messages.md) | GET |  |
| [CrashAnalytics get Crash Summary](actions/crash-analytics-get-crash-summary.md) | GET |  |
| [CrashAnalytics get Crash Types](actions/crash-analytics-get-crash-types.md) | GET |  |
| [CrashAnalytics get Crash Visit Context](actions/crash-analytics-get-crash-visit-context.md) | GET |  |
| [CrashAnalytics get Crashes By Category](actions/crash-analytics-get-crashes-by-category.md) | GET |  |
| [CrashAnalytics get Crashes By First Party](actions/crash-analytics-get-crashes-by-first-party.md) | GET |  |
| [CrashAnalytics get Crashes By Page Title](actions/crash-analytics-get-crashes-by-page-title.md) | GET |  |
| [CrashAnalytics get Crashes By Page Url](actions/crash-analytics-get-crashes-by-page-url.md) | GET |  |
| [CrashAnalytics get Crashes By Source](actions/crash-analytics-get-crashes-by-source.md) | GET |  |
| [CrashAnalytics get Crashes By Third Party](actions/crash-analytics-get-crashes-by-third-party.md) | GET |  |
| [CrashAnalytics get Crashes For Category](actions/crash-analytics-get-crashes-for-category.md) | GET |  |
| [CrashAnalytics get Crashes For Page Title](actions/crash-analytics-get-crashes-for-page-title.md) | GET |  |
| [CrashAnalytics get Crashes For Page Url](actions/crash-analytics-get-crashes-for-page-url.md) | GET |  |
| [CrashAnalytics get Crashes For Source](actions/crash-analytics-get-crashes-for-source.md) | GET |  |
| [CrashAnalytics get Disappeared Crashes](actions/crash-analytics-get-disappeared-crashes.md) | GET |  |
| [CrashAnalytics get Ignored Crashes](actions/crash-analytics-get-ignored-crashes.md) | GET |  |
| [CrashAnalytics get Last Crashes Overview](actions/crash-analytics-get-last-crashes-overview.md) | GET |  |
| [CrashAnalytics get Last Disappeared Crashes](actions/crash-analytics-get-last-disappeared-crashes.md) | GET |  |
| [CrashAnalytics get Last New Crashes](actions/crash-analytics-get-last-new-crashes.md) | GET |  |
| [CrashAnalytics get Last Reappeared Crashes](actions/crash-analytics-get-last-reappeared-crashes.md) | GET |  |
| [CrashAnalytics get Last Top Crashes](actions/crash-analytics-get-last-top-crashes.md) | GET |  |
| [CrashAnalytics get New Crashes](actions/crash-analytics-get-new-crashes.md) | GET |  |
| [CrashAnalytics get Reappeared Crashes](actions/crash-analytics-get-reappeared-crashes.md) | GET |  |
| [CrashAnalytics get Unidentified Crash Messages](actions/crash-analytics-get-unidentified-crash-messages.md) | GET |  |
| [CrashAnalytics merge Crashes](actions/crash-analytics-merge-crashes.md) | GET |  |
| [CrashAnalytics search Crash Messages For Merge](actions/crash-analytics-search-crash-messages-for-merge.md) | GET |  |
| [CrashAnalytics set Ignore Crash](actions/crash-analytics-set-ignore-crash.md) | PUT |  |
| [CrashAnalytics unmerge Crash Group](actions/crash-analytics-unmerge-crash-group.md) | GET |  |

### Customalerts

| Action | Method | Description |
| --- | --- | --- |
| [CustomAlerts add Alert](actions/custom-alerts-add-alert.md) | POST |  |
| [CustomAlerts delete Alert](actions/custom-alerts-delete-alert.md) | DELETE |  |
| [CustomAlerts edit Alert](actions/custom-alerts-edit-alert.md) | GET |  |
| [CustomAlerts get Alert](actions/custom-alerts-get-alert.md) | GET |  |
| [CustomAlerts get Alerts](actions/custom-alerts-get-alerts.md) | GET |  |
| [CustomAlerts get Triggered Alerts](actions/custom-alerts-get-triggered-alerts.md) | GET |  |
| [CustomAlerts get Values For Alert In Past](actions/custom-alerts-get-values-for-alert-in-past.md) | GET |  |

### Customdimensions

| Action | Method | Description |
| --- | --- | --- |
| [CustomDimensions configure Existing Custom Dimension](actions/custom-dimensions-configure-existing-custom-dimension.md) | GET |  |
| [CustomDimensions configure New Custom Dimension](actions/custom-dimensions-configure-new-custom-dimension.md) | GET |  |
| [CustomDimensions get Available Extraction Dimensions](actions/custom-dimensions-get-available-extraction-dimensions.md) | GET |  |
| [CustomDimensions get Available Scopes](actions/custom-dimensions-get-available-scopes.md) | GET |  |
| [CustomDimensions get Configured Custom Dimensions](actions/custom-dimensions-get-configured-custom-dimensions.md) | GET |  |
| [CustomDimensions get Configured Custom Dimensions Having Scope](actions/custom-dimensions-get-configured-custom-dimensions-having-scope.md) | GET |  |
| [CustomDimensions get Custom Dimension](actions/custom-dimensions-get-custom-dimension.md) | GET |  |

### Customjstracker

| Action | Method | Description |
| --- | --- | --- |
| [CustomJsTracker does Include Plugin Trackers Automatically](actions/custom-js-tracker-does-include-plugin-trackers-automatically.md) | GET |  |

### Customreports

| Action | Method | Description |
| --- | --- | --- |
| [CustomReports add Custom Report](actions/custom-reports-add-custom-report.md) | POST |  |
| [CustomReports delete Custom Report](actions/custom-reports-delete-custom-report.md) | DELETE |  |
| [CustomReports duplicate Custom Report](actions/custom-reports-duplicate-custom-report.md) | GET |  |
| [CustomReports get Available Categories](actions/custom-reports-get-available-categories.md) | GET |  |
| [CustomReports get Available Dimensions](actions/custom-reports-get-available-dimensions.md) | GET |  |
| [CustomReports get Available Metrics](actions/custom-reports-get-available-metrics.md) | GET |  |
| [CustomReports get Available Report Types](actions/custom-reports-get-available-report-types.md) | GET |  |
| [CustomReports get Configured Report](actions/custom-reports-get-configured-report.md) | GET |  |
| [CustomReports get Configured Reports](actions/custom-reports-get-configured-reports.md) | GET |  |
| [CustomReports get Custom Report](actions/custom-reports-get-custom-report.md) | GET |  |
| [CustomReports pause Custom Report](actions/custom-reports-pause-custom-report.md) | GET |  |
| [CustomReports resume Custom Report](actions/custom-reports-resume-custom-report.md) | GET |  |
| [CustomReports update Custom Report](actions/custom-reports-update-custom-report.md) | PUT |  |

### Customvariables

| Action | Method | Description |
| --- | --- | --- |
| [CustomVariables get Custom Variables](actions/custom-variables-get-custom-variables.md) | GET |  |
| [CustomVariables get Custom Variables Values From Name Id](actions/custom-variables-get-custom-variables-values-from-name-id.md) | GET |  |
| [CustomVariables get Usages Of Slots](actions/custom-variables-get-usages-of-slots.md) | GET |  |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Dashboard copy Dashboard To User](actions/dashboard-copy-dashboard-to-user.md) | GET |  |
| [Dashboard create New Dashboard For User](actions/dashboard-create-new-dashboard-for-user.md) | POST |  |
| [Dashboard get Dashboards](actions/dashboard-get-dashboards.md) | GET |  |
| [Dashboard remove Dashboard](actions/dashboard-remove-dashboard.md) | DELETE |  |
| [Dashboard reset Dashboard Layout](actions/dashboard-reset-dashboard-layout.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Events get Action From Category Id](actions/events-get-action-from-category-id.md) | GET |  |
| [Events get Action From Name Id](actions/events-get-action-from-name-id.md) | GET |  |
| [Events get Category From Action Id](actions/events-get-category-from-action-id.md) | GET |  |
| [Events get Category From Name Id](actions/events-get-category-from-name-id.md) | GET |  |
| [Events get Name From Action Id](actions/events-get-name-from-action-id.md) | GET |  |
| [Events get Name From Category Id](actions/events-get-name-from-category-id.md) | GET |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Feedback send Feedback For Feature](actions/feedback-send-feedback-for-feature.md) | GET |  |
| [Feedback send Feedback For Survey](actions/feedback-send-feedback-for-survey.md) | GET |  |
| [Feedback update Feedback Reminder Date](actions/feedback-update-feedback-reminder-date.md) | PUT |  |

### Formanalytics

| Action | Method | Description |
| --- | --- | --- |
| [FormAnalytics add Form](actions/form-analytics-add-form.md) | POST |  |
| [FormAnalytics archive Form](actions/form-analytics-archive-form.md) | DELETE |  |
| [FormAnalytics delete Form](actions/form-analytics-delete-form.md) | DELETE |  |
| [FormAnalytics get All Goals](actions/form-analytics-get-all-goals.md) | GET |  |
| [FormAnalytics get Auto Creation Settings](actions/form-analytics-get-auto-creation-settings.md) | GET |  |
| [FormAnalytics get Available Conversion Rule Options](actions/form-analytics-get-available-conversion-rule-options.md) | GET |  |
| [FormAnalytics get Available Form Rules](actions/form-analytics-get-available-form-rules.md) | GET |  |
| [FormAnalytics get Available Page Rules](actions/form-analytics-get-available-page-rules.md) | GET |  |
| [FormAnalytics get Available Statuses](actions/form-analytics-get-available-statuses.md) | GET |  |
| [FormAnalytics get Counters](actions/form-analytics-get-counters.md) | GET |  |
| [FormAnalytics get Current Most Popular Forms](actions/form-analytics-get-current-most-popular-forms.md) | GET |  |
| [FormAnalytics get Drop Off Fields](actions/form-analytics-get-drop-off-fields.md) | GET |  |
| [FormAnalytics get Entry Fields](actions/form-analytics-get-entry-fields.md) | GET |  |
| [FormAnalytics get Field Corrections](actions/form-analytics-get-field-corrections.md) | GET |  |
| [FormAnalytics get Field Size](actions/form-analytics-get-field-size.md) | GET |  |
| [FormAnalytics get Field Timings](actions/form-analytics-get-field-timings.md) | GET |  |
| [FormAnalytics get Form](actions/form-analytics-get-form.md) | GET |  |
| [FormAnalytics get Forms](actions/form-analytics-get-forms.md) | GET |  |
| [FormAnalytics get Forms By Statuses](actions/form-analytics-get-forms-by-statuses.md) | GET |  |
| [FormAnalytics get Most Used Fields](actions/form-analytics-get-most-used-fields.md) | GET |  |
| [FormAnalytics get Page Urls](actions/form-analytics-get-page-urls.md) | GET |  |
| [FormAnalytics get Uneeded Fields](actions/form-analytics-get-uneeded-fields.md) | GET |  |
| [FormAnalytics update Form](actions/form-analytics-update-form.md) | PUT |  |
| [FormAnalytics update Form Field Display Name](actions/form-analytics-update-form-field-display-name.md) | PUT |  |

### Funnels

| Action | Method | Description |
| --- | --- | --- |
| [Funnels delete Goal Funnel](actions/funnels-delete-goal-funnel.md) | DELETE |  |
| [Funnels delete Non Goal Funnel](actions/funnels-delete-non-goal-funnel.md) | DELETE |  |
| [Funnels get All Activated Funnels For Site](actions/funnels-get-all-activated-funnels-for-site.md) | GET |  |
| [Funnels get Available Pattern Matches](actions/funnels-get-available-pattern-matches.md) | GET |  |
| [Funnels get Funnel](actions/funnels-get-funnel.md) | GET |  |
| [Funnels get Funnel Entries](actions/funnels-get-funnel-entries.md) | GET |  |
| [Funnels get Funnel Exits](actions/funnels-get-funnel-exits.md) | GET |  |
| [Funnels get Funnel Flow](actions/funnels-get-funnel-flow.md) | GET |  |
| [Funnels get Funnel Flow Table](actions/funnels-get-funnel-flow-table.md) | GET |  |
| [Funnels get Funnel Step Subtable](actions/funnels-get-funnel-step-subtable.md) | GET |  |
| [Funnels get Goal Funnel](actions/funnels-get-goal-funnel.md) | GET |  |
| [Funnels get Metrics](actions/funnels-get-metrics.md) | GET |  |
| [Funnels get Sales Funnel For Site](actions/funnels-get-sales-funnel-for-site.md) | GET |  |
| [Funnels has Any Activated Funnel For Site](actions/funnels-has-any-activated-funnel-for-site.md) | GET |  |
| [Funnels save Non Goal Funnel](actions/funnels-save-non-goal-funnel.md) | GET |  |
| [Funnels set Goal Funnel](actions/funnels-set-goal-funnel.md) | PUT |  |
| [Funnels test Url Matches Steps](actions/funnels-test-url-matches-steps.md) | GET |  |

### Goals

| Action | Method | Description |
| --- | --- | --- |
| [Goals add Goal](actions/goals-add-goal.md) | POST |  |
| [Goals delete Goal](actions/goals-delete-goal.md) | DELETE |  |
| [Goals get Goal](actions/goals-get-goal.md) | GET |  |
| [Goals get Goals](actions/goals-get-goals.md) | GET |  |
| [Goals update Goal](actions/goals-update-goal.md) | PUT |  |

### Heatmapsessionrecording

| Action | Method | Description |
| --- | --- | --- |
| [HeatmapSessionRecording add Heatmap](actions/heatmap-session-recording-add-heatmap.md) | POST |  |
| [HeatmapSessionRecording add Session Recording](actions/heatmap-session-recording-add-session-recording.md) | POST |  |
| [HeatmapSessionRecording delete Heatmap](actions/heatmap-session-recording-delete-heatmap.md) | DELETE |  |
| [HeatmapSessionRecording delete Heatmap Screenshot](actions/heatmap-session-recording-delete-heatmap-screenshot.md) | DELETE |  |
| [HeatmapSessionRecording delete Recorded Pageview](actions/heatmap-session-recording-delete-recorded-pageview.md) | DELETE |  |
| [HeatmapSessionRecording delete Recorded Session](actions/heatmap-session-recording-delete-recorded-session.md) | DELETE |  |
| [HeatmapSessionRecording delete Session Recording](actions/heatmap-session-recording-delete-session-recording.md) | DELETE |  |
| [HeatmapSessionRecording duplicate Heatmap](actions/heatmap-session-recording-duplicate-heatmap.md) | POST |  |
| [HeatmapSessionRecording end Heatmap](actions/heatmap-session-recording-end-heatmap.md) | PUT |  |
| [HeatmapSessionRecording end Session Recording](actions/heatmap-session-recording-end-session-recording.md) | PUT |  |
| [HeatmapSessionRecording get Available Device Types](actions/heatmap-session-recording-get-available-device-types.md) | GET |  |
| [HeatmapSessionRecording get Available Heatmap Types](actions/heatmap-session-recording-get-available-heatmap-types.md) | GET |  |
| [HeatmapSessionRecording get Available Session Recording Sample Limits](actions/heatmap-session-recording-get-available-session-recording-sample-limits.md) | GET |  |
| [HeatmapSessionRecording get Available Statuses](actions/heatmap-session-recording-get-available-statuses.md) | GET |  |
| [HeatmapSessionRecording get Available Target Page Rules](actions/heatmap-session-recording-get-available-target-page-rules.md) | GET |  |
| [HeatmapSessionRecording get Embed Session Info](actions/heatmap-session-recording-get-embed-session-info.md) | GET |  |
| [HeatmapSessionRecording get Event Types](actions/heatmap-session-recording-get-event-types.md) | GET |  |
| [HeatmapSessionRecording get Heatmap](actions/heatmap-session-recording-get-heatmap.md) | GET |  |
| [HeatmapSessionRecording get Heatmaps](actions/heatmap-session-recording-get-heatmaps.md) | GET |  |
| [HeatmapSessionRecording get Recorded Heatmap](actions/heatmap-session-recording-get-recorded-heatmap.md) | GET |  |
| [HeatmapSessionRecording get Recorded Heatmap Metadata](actions/heatmap-session-recording-get-recorded-heatmap-metadata.md) | GET |  |
| [HeatmapSessionRecording get Recorded Session](actions/heatmap-session-recording-get-recorded-session.md) | GET |  |
| [HeatmapSessionRecording get Recorded Sessions](actions/heatmap-session-recording-get-recorded-sessions.md) | GET |  |
| [HeatmapSessionRecording get Session Recording](actions/heatmap-session-recording-get-session-recording.md) | GET |  |
| [HeatmapSessionRecording get Session Recordings](actions/heatmap-session-recording-get-session-recordings.md) | GET |  |
| [HeatmapSessionRecording pause Heatmap](actions/heatmap-session-recording-pause-heatmap.md) | PUT |  |
| [HeatmapSessionRecording pause Session Recording](actions/heatmap-session-recording-pause-session-recording.md) | PUT |  |
| [HeatmapSessionRecording resume Heatmap](actions/heatmap-session-recording-resume-heatmap.md) | PUT |  |
| [HeatmapSessionRecording resume Session Recording](actions/heatmap-session-recording-resume-session-recording.md) | PUT |  |
| [HeatmapSessionRecording test Url Match Pages](actions/heatmap-session-recording-test-url-match-pages.md) | GET |  |
| [HeatmapSessionRecording update Heatmap](actions/heatmap-session-recording-update-heatmap.md) | PUT |  |
| [HeatmapSessionRecording update Session Recording](actions/heatmap-session-recording-update-session-recording.md) | PUT |  |

### Imagegraph

| Action | Method | Description |
| --- | --- | --- |
| [ImageGraph get](actions/image-graph-get.md) | GET |  |

### Insights

| Action | Method | Description |
| --- | --- | --- |
| [Insights can Generate Insights](actions/insights-can-generate-insights.md) | GET |  |
| [Insights get Insights](actions/insights-get-insights.md) | GET |  |
| [Insights get Insights Overview](actions/insights-get-insights-overview.md) | GET |  |
| [Insights get Movers And Shakers](actions/insights-get-movers-and-shakers.md) | GET |  |
| [Insights get Movers And Shakers Overview](actions/insights-get-movers-and-shakers-overview.md) | GET |  |

### Languagesmanager

| Action | Method | Description |
| --- | --- | --- |
| [LanguagesManager get Available Language Names](actions/languages-manager-get-available-language-names.md) | GET |  |
| [LanguagesManager get Available Languages](actions/languages-manager-get-available-languages.md) | GET |  |
| [LanguagesManager get Available Languages Info](actions/languages-manager-get-available-languages-info.md) | GET |  |
| [LanguagesManager get Language For User](actions/languages-manager-get-language-for-user.md) | GET |  |
| [LanguagesManager get Translations For Language](actions/languages-manager-get-translations-for-language.md) | GET |  |
| [LanguagesManager is Language Available](actions/languages-manager-is-language-available.md) | GET |  |
| [LanguagesManager set Language For User](actions/languages-manager-set-language-for-user.md) | PUT |  |
| [LanguagesManager set12 Hour Clock For User](actions/languages-manager-set12-hour-clock-for-user.md) | PUT |  |
| [LanguagesManager uses12 Hour Clock For User](actions/languages-manager-uses12-hour-clock-for-user.md) | GET |  |

### Live

| Action | Method | Description |
| --- | --- | --- |
| [Live get Counters](actions/live-get-counters.md) | GET |  |
| [Live get Last Visits Details](actions/live-get-last-visits-details.md) | GET |  |
| [Live get Most Recent Visitor Id](actions/live-get-most-recent-visitor-id.md) | GET |  |
| [Live get Most Recent Visits Date Time](actions/live-get-most-recent-visits-date-time.md) | GET |  |
| [Live get Visitor Profile](actions/live-get-visitor-profile.md) | GET |  |
| [Live is Visitor Profile Enabled](actions/live-is-visitor-profile-enabled.md) | GET |  |

### Login

| Action | Method | Description |
| --- | --- | --- |
| [Login unblock Brute Force IPs](actions/login-unblock-brute-force-i-ps.md) | GET |  |

### Marketingcampaignsreporting

| Action | Method | Description |
| --- | --- | --- |
| [MarketingCampaignsReporting get Keyword Content From Name Id](actions/marketing-campaigns-reporting-get-keyword-content-from-name-id.md) | GET |  |
| [MarketingCampaignsReporting get Name From Source Medium Id](actions/marketing-campaigns-reporting-get-name-from-source-medium-id.md) | GET |  |

### Matomo Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Matomo Version](actions/get-matomo-version.md) | GET |  |

### Mediaanalytics

| Action | Method | Description |
| --- | --- | --- |
| [MediaAnalytics get Current Most Plays](actions/media-analytics-get-current-most-plays.md) | GET |  |
| [MediaAnalytics get Current Num Plays](actions/media-analytics-get-current-num-plays.md) | GET |  |
| [MediaAnalytics get Current Sum Time Spent](actions/media-analytics-get-current-sum-time-spent.md) | GET |  |
| [MediaAnalytics has Records](actions/media-analytics-has-records.md) | GET |  |

### Mobilemessaging

| Action | Method | Description |
| --- | --- | --- |
| [MobileMessaging add Phone Number](actions/mobile-messaging-add-phone-number.md) | POST |  |
| [MobileMessaging are SMSAPICredential Provided](actions/mobile-messaging-are-smsapi-credential-provided.md) | GET |  |
| [MobileMessaging delete SMSAPICredential](actions/mobile-messaging-delete-smsapi-credential.md) | DELETE |  |
| [MobileMessaging get Credit Left](actions/mobile-messaging-get-credit-left.md) | GET |  |
| [MobileMessaging get Delegated Management](actions/mobile-messaging-get-delegated-management.md) | GET |  |
| [MobileMessaging get Phone Numbers](actions/mobile-messaging-get-phone-numbers.md) | GET |  |
| [MobileMessaging get SMSProvider](actions/mobile-messaging-get-sms-provider.md) | GET |  |
| [MobileMessaging remove Phone Number](actions/mobile-messaging-remove-phone-number.md) | DELETE |  |
| [MobileMessaging resend Verification Code](actions/mobile-messaging-resend-verification-code.md) | GET |  |
| [MobileMessaging set Delegated Management](actions/mobile-messaging-set-delegated-management.md) | PUT |  |
| [MobileMessaging set SMSAPICredential](actions/mobile-messaging-set-smsapi-credential.md) | PUT |  |
| [MobileMessaging validate Phone Number](actions/mobile-messaging-validate-phone-number.md) | GET |  |

### Multichannelconversionattribution

| Action | Method | Description |
| --- | --- | --- |
| [MultiChannelConversionAttribution get Available Campaign Dimension Combinations](actions/multi-channel-conversion-attribution-get-available-campaign-dimension-combinations.md) | GET |  |
| [MultiChannelConversionAttribution get Channel Attribution](actions/multi-channel-conversion-attribution-get-channel-attribution.md) | GET |  |
| [MultiChannelConversionAttribution get Goal Attribution](actions/multi-channel-conversion-attribution-get-goal-attribution.md) | GET |  |
| [MultiChannelConversionAttribution get Site Attribution Goals](actions/multi-channel-conversion-attribution-get-site-attribution-goals.md) | GET |  |
| [MultiChannelConversionAttribution set Goal Attribution](actions/multi-channel-conversion-attribution-set-goal-attribution.md) | PUT |  |

### Multisites

| Action | Method | Description |
| --- | --- | --- |
| [MultiSites get All With Groups](actions/multi-sites-get-all-with-groups.md) | GET |  |

### Oauth2

| Action | Method | Description |
| --- | --- | --- |
| [OAuth2 create Client](actions/o-auth2-create-client.md) | POST |  |
| [OAuth2 delete Client](actions/o-auth2-delete-client.md) | DELETE |  |
| [OAuth2 get Client](actions/o-auth2-get-client.md) | GET |  |
| [OAuth2 get Clients](actions/o-auth2-get-clients.md) | GET |  |
| [OAuth2 get Scopes](actions/o-auth2-get-scopes.md) | GET |  |
| [OAuth2 rotate Secret](actions/o-auth2-rotate-secret.md) | GET |  |
| [OAuth2 set Client Active](actions/o-auth2-set-client-active.md) | PUT |  |
| [OAuth2 update Client](actions/o-auth2-update-client.md) | PUT |  |

### Openapidocs

| Action | Method | Description |
| --- | --- | --- |
| [OpenApiDocs get Generated Open Api Spec](actions/open-api-docs-get-generated-open-api-spec.md) | GET |  |
| [OpenApiDocs get Open Api Spec](actions/open-api-docs-get-open-api-spec.md) | GET |  |
| [OpenApiDocs get Plugin Whitelist](actions/open-api-docs-get-plugin-whitelist.md) | GET |  |

### Overlay

| Action | Method | Description |
| --- | --- | --- |
| [Overlay get Following Pages](actions/overlay-get-following-pages.md) | GET |  |
| [Overlay get Translations](actions/overlay-get-translations.md) | GET |  |

### Privacymanager

| Action | Method | Description |
| --- | --- | --- |
| [PrivacyManager anonymize Some Raw Data](actions/privacy-manager-anonymize-some-raw-data.md) | GET |  |
| [PrivacyManager delete Data Subjects](actions/privacy-manager-delete-data-subjects.md) | DELETE |  |
| [PrivacyManager export Data Subjects](actions/privacy-manager-export-data-subjects.md) | GET |  |
| [PrivacyManager find Data Subjects](actions/privacy-manager-find-data-subjects.md) | GET |  |
| [PrivacyManager get Available Link Visit Action Columns To Anonymize](actions/privacy-manager-get-available-link-visit-action-columns-to-anonymize.md) | GET |  |
| [PrivacyManager get Available Visit Columns To Anonymize](actions/privacy-manager-get-available-visit-columns-to-anonymize.md) | GET |  |

### Referrers

| Action | Method | Description |
| --- | --- | --- |
| [Referrers get Campaigns](actions/referrers-get-campaigns.md) | GET |  |
| [Referrers get Entry Page Titles For AIAssistant](actions/referrers-get-entry-page-titles-for-ai-assistant.md) | GET |  |
| [Referrers get Entry Page Urls For AIAssistant](actions/referrers-get-entry-page-urls-for-ai-assistant.md) | GET |  |
| [Referrers get Keywords From Campaign Id](actions/referrers-get-keywords-from-campaign-id.md) | GET |  |
| [Referrers get Keywords From Search Engine Id](actions/referrers-get-keywords-from-search-engine-id.md) | GET |  |
| [Referrers get Number Of Distinct AIAssistants](actions/referrers-get-number-of-distinct-ai-assistants.md) | GET |  |
| [Referrers get Number Of Distinct Campaigns](actions/referrers-get-number-of-distinct-campaigns.md) | GET |  |
| [Referrers get Number Of Distinct Keywords](actions/referrers-get-number-of-distinct-keywords.md) | GET |  |
| [Referrers get Number Of Distinct Search Engines](actions/referrers-get-number-of-distinct-search-engines.md) | GET |  |
| [Referrers get Number Of Distinct Social Networks](actions/referrers-get-number-of-distinct-social-networks.md) | GET |  |
| [Referrers get Number Of Distinct Websites](actions/referrers-get-number-of-distinct-websites.md) | GET |  |
| [Referrers get Number Of Distinct Websites Urls](actions/referrers-get-number-of-distinct-websites-urls.md) | GET |  |
| [Referrers get Search Engines From Keyword Id](actions/referrers-get-search-engines-from-keyword-id.md) | GET |  |
| [Referrers get Urls For Social](actions/referrers-get-urls-for-social.md) | GET |  |
| [Referrers get Urls From Website Id](actions/referrers-get-urls-from-website-id.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Actions - Main metrics](actions/actions-get.md) | GET |  |
| [Get Downloads](actions/actions-get-downloads.md) | GET |  |
| [Get Entry page titles](actions/actions-get-entry-page-titles.md) | GET |  |
| [Get Entry pages](actions/actions-get-entry-page-urls.md) | GET |  |
| [Get Exit page titles](actions/actions-get-exit-page-titles.md) | GET |  |
| [Get Exit pages](actions/actions-get-exit-page-urls.md) | GET |  |
| [Get Outlinks](actions/actions-get-outlinks.md) | GET |  |
| [Get Page titles](actions/actions-get-page-titles.md) | GET |  |
| [Get Page Titles Following a Site Search](actions/actions-get-page-titles-following-site-search.md) | GET |  |
| [Get Page URLs](actions/actions-get-page-urls.md) | GET |  |
| [Get Pages Following a Site Search](actions/actions-get-page-urls-following-site-search.md) | GET |  |
| [Get Search Categories](actions/actions-get-site-search-categories.md) | GET |  |
| [Get Site Search Keywords](actions/actions-get-site-search-keywords.md) | GET |  |
| [Get Search Keywords with No Results](actions/actions-get-site-search-no-result-keywords.md) | GET |  |
| [Get AI Agent Visits](actions/ai-agents-get.md) | GET |  |
| [Get Main Metrics](actions/api-get.md) | GET |  |
| [Get AI Chatbots Overview](actions/bot-tracking-get.md) | GET |  |
| [Get AI Chatbots](actions/bot-tracking-get-ai-chatbot-requests.md) | GET |  |
| [Get Content Name](actions/contents-get-content-names.md) | GET |  |
| [Get Content Piece](actions/contents-get-content-pieces.md) | GET |  |
| [Get Browser Plugins](actions/device-plugins-get-plugin.md) | GET |  |
| [Get Device brand](actions/devices-detection-get-brand.md) | GET |  |
| [Get Browser engines](actions/devices-detection-get-browser-engines.md) | GET |  |
| [Get Browser version](actions/devices-detection-get-browser-versions.md) | GET |  |
| [Get Browsers](actions/devices-detection-get-browsers.md) | GET |  |
| [Get Device model](actions/devices-detection-get-model.md) | GET |  |
| [Get Operating System families](actions/devices-detection-get-os-families.md) | GET |  |
| [Get Operating System versions](actions/devices-detection-get-os-versions.md) | GET |  |
| [Get Device type](actions/devices-detection-get-type.md) | GET |  |
| [Get Event Actions](actions/events-get-action.md) | GET |  |
| [Get Event Categories](actions/events-get-category.md) | GET |  |
| [Get Event Names](actions/events-get-name.md) | GET |  |
| [Get Forms Overview](actions/form-analytics-get.md) | GET |  |
| [Get Ecommerce Orders](actions/goals-get.md) | GET |  |
| [Get Ecommerce Orders - Days to Conversion](actions/goals-get-days-to-conversion.md) | GET |  |
| [Get Product Category](actions/goals-get-items-category.md) | GET |  |
| [Get Product Name](actions/goals-get-items-name.md) | GET |  |
| [Get Product SKU](actions/goals-get-items-sku.md) | GET |  |
| [Get Ecommerce Orders - Visits to Conversion](actions/goals-get-visits-until-conversion.md) | GET |  |
| [Get Campaign Contents](actions/marketing-campaigns-reporting-get-content.md) | GET |  |
| [Get Campaign Groups](actions/marketing-campaigns-reporting-get-group.md) | GET |  |
| [Get Campaign Ids](actions/marketing-campaigns-reporting-get-id.md) | GET |  |
| [Get Campaign Keywords](actions/marketing-campaigns-reporting-get-keyword.md) | GET |  |
| [Get Campaign Mediums](actions/marketing-campaigns-reporting-get-medium.md) | GET |  |
| [Get Campaign Names](actions/marketing-campaigns-reporting-get-name.md) | GET |  |
| [Get Campaign Placements](actions/marketing-campaigns-reporting-get-placement.md) | GET |  |
| [Get Campaign Sources](actions/marketing-campaigns-reporting-get-source.md) | GET |  |
| [Get Campaign Source - Medium](actions/marketing-campaigns-reporting-get-source-medium.md) | GET |  |
| [Get Media Summary](actions/media-analytics-get.md) | GET |  |
| [Get Audio per hour in website timezone](actions/media-analytics-get-audio-hours.md) | GET |  |
| [Get Audio Resource URLs](actions/media-analytics-get-audio-resources.md) | GET |  |
| [Get Audio Titles](actions/media-analytics-get-audio-titles.md) | GET |  |
| [Get Audio Resources URLs Grouped](actions/media-analytics-get-grouped-audio-resources.md) | GET |  |
| [Get Video Resource URLs Grouped](actions/media-analytics-get-grouped-video-resources.md) | GET |  |
| [Get Media Players](actions/media-analytics-get-players.md) | GET |  |
| [Get Videos per hour in website's timezone](actions/media-analytics-get-video-hours.md) | GET |  |
| [Get Video Resolutions](actions/media-analytics-get-video-resolutions.md) | GET |  |
| [Get Video Resource URLs](actions/media-analytics-get-video-resources.md) | GET |  |
| [Get Video Titles](actions/media-analytics-get-video-titles.md) | GET |  |
| [Get All Websites dashboard](actions/multi-sites-get-all.md) | GET |  |
| [Get Single Website dashboard](actions/multi-sites-get-one.md) | GET |  |
| [Get Performance overview](actions/page-performance-get.md) | GET |  |
| [Get Referrers Overview](actions/referrers-get.md) | GET |  |
| [Get AI Assistants](actions/referrers-get-ai-assistants.md) | GET |  |
| [Get All Channels](actions/referrers-get-all.md) | GET |  |
| [Get Keywords](actions/referrers-get-keywords.md) | GET |  |
| [Get Channel Type](actions/referrers-get-referrer-type.md) | GET |  |
| [Get Search Engines](actions/referrers-get-search-engines.md) | GET |  |
| [Get Social Networks](actions/referrers-get-socials.md) | GET |  |
| [Get Websites](actions/referrers-get-websites.md) | GET |  |
| [Get Configurations](actions/resolution-get-configuration.md) | GET |  |
| [Get Screen Resolution](actions/resolution-get-resolution.md) | GET |  |
| [Get City](actions/user-country-get-city.md) | GET |  |
| [Get Continent](actions/user-country-get-continent.md) | GET |  |
| [Get Country](actions/user-country-get-country.md) | GET |  |
| [Get Region](actions/user-country-get-region.md) | GET |  |
| [Get User IDs](actions/user-id-get-users.md) | GET |  |
| [Get Web-browser language](actions/user-language-get-language.md) | GET |  |
| [Get Language code](actions/user-language-get-language-code.md) | GET |  |
| [Get Users Flow](actions/users-flow-get-users-flow-pretty.md) | GET |  |
| [Get Returning Visits](actions/visit-frequency-get.md) | GET |  |
| [Get Visits by day of the week](actions/visit-time-get-by-day-of-week.md) | GET |  |
| [Get Visits per local time](actions/visit-time-get-visit-information-per-local-time.md) | GET |  |
| [Get Visits per hour in the site's timezone](actions/visit-time-get-visit-information-per-server-time.md) | GET |  |
| [Get Visits by days since last visit](actions/visitor-interest-get-number-of-visits-by-days-since-last.md) | GET |  |
| [Get Visits by visit number](actions/visitor-interest-get-number-of-visits-by-visit-count.md) | GET |  |
| [Get Pages per visit](actions/visitor-interest-get-number-of-visits-per-page.md) | GET |  |
| [Get Length of visits](actions/visitor-interest-get-number-of-visits-per-visit-duration.md) | GET |  |
| [Get Visits Summary](actions/visits-summary-get.md) | GET |  |

### Rollupreporting

| Action | Method | Description |
| --- | --- | --- |
| [RollUpReporting add Roll Up](actions/roll-up-reporting-add-roll-up.md) | POST |  |
| [RollUpReporting get Roll Ups](actions/roll-up-reporting-get-roll-ups.md) | GET |  |
| [RollUpReporting update Roll Up](actions/roll-up-reporting-update-roll-up.md) | PUT |  |

### Scheduledreports

| Action | Method | Description |
| --- | --- | --- |
| [ScheduledReports add Report](actions/scheduled-reports-add-report.md) | POST |  |
| [ScheduledReports delete Report](actions/scheduled-reports-delete-report.md) | DELETE |  |
| [ScheduledReports generate Report](actions/scheduled-reports-generate-report.md) | GET |  |
| [ScheduledReports get Reports](actions/scheduled-reports-get-reports.md) | GET |  |
| [ScheduledReports send Report](actions/scheduled-reports-send-report.md) | GET |  |
| [ScheduledReports update Report](actions/scheduled-reports-update-report.md) | PUT |  |

### Searchenginekeywordsperformance

| Action | Method | Description |
| --- | --- | --- |
| [SearchEngineKeywordsPerformance get Crawling Error Examples Bing](actions/search-engine-keywords-performance-get-crawling-error-examples-bing.md) | GET |  |
| [SearchEngineKeywordsPerformance get Crawling Overview Bing](actions/search-engine-keywords-performance-get-crawling-overview-bing.md) | GET |  |
| [SearchEngineKeywordsPerformance get Crawling Overview Yandex](actions/search-engine-keywords-performance-get-crawling-overview-yandex.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords](actions/search-engine-keywords-performance-get-keywords.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Bing](actions/search-engine-keywords-performance-get-keywords-bing.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Google](actions/search-engine-keywords-performance-get-keywords-google.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Google Image](actions/search-engine-keywords-performance-get-keywords-google-image.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Google News](actions/search-engine-keywords-performance-get-keywords-google-news.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Google Video](actions/search-engine-keywords-performance-get-keywords-google-video.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Google Web](actions/search-engine-keywords-performance-get-keywords-google-web.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Imported](actions/search-engine-keywords-performance-get-keywords-imported.md) | GET |  |
| [SearchEngineKeywordsPerformance get Keywords Yandex](actions/search-engine-keywords-performance-get-keywords-yandex.md) | GET |  |

### Segmenteditor

| Action | Method | Description |
| --- | --- | --- |
| [SegmentEditor add](actions/segment-editor-add.md) | POST |  |
| [SegmentEditor delete](actions/segment-editor-delete.md) | DELETE |  |
| [SegmentEditor get](actions/segment-editor-get.md) | GET |  |
| [SegmentEditor get All](actions/segment-editor-get-all.md) | GET |  |
| [SegmentEditor get Segment Data](actions/segment-editor-get-segment-data.md) | GET |  |
| [SegmentEditor is User Can Add New Segment](actions/segment-editor-is-user-can-add-new-segment.md) | GET |  |
| [SegmentEditor star](actions/segment-editor-star.md) | GET |  |
| [SegmentEditor unstar](actions/segment-editor-unstar.md) | GET |  |
| [SegmentEditor update](actions/segment-editor-update.md) | PUT |  |

### Seo

| Action | Method | Description |
| --- | --- | --- |
| [SEO get Rank](actions/s-eo-get-rank.md) | GET |  |

### Sitesmanager

| Action | Method | Description |
| --- | --- | --- |
| [SitesManager add Site](actions/sites-manager-add-site.md) | POST |  |
| [SitesManager add Site Alias Urls](actions/sites-manager-add-site-alias-urls.md) | POST |  |
| [SitesManager delete Site](actions/sites-manager-delete-site.md) | DELETE |  |
| [SitesManager get All Sites](actions/sites-manager-get-all-sites.md) | GET |  |
| [SitesManager get All Sites Id](actions/sites-manager-get-all-sites-id.md) | GET |  |
| [SitesManager get Currency List](actions/sites-manager-get-currency-list.md) | GET |  |
| [SitesManager get Currency Symbols](actions/sites-manager-get-currency-symbols.md) | GET |  |
| [SitesManager get Default Currency](actions/sites-manager-get-default-currency.md) | GET |  |
| [SitesManager get Default Timezone](actions/sites-manager-get-default-timezone.md) | GET |  |
| [SitesManager get Excluded Ips Global](actions/sites-manager-get-excluded-ips-global.md) | GET |  |
| [SitesManager get Excluded Query Parameters](actions/sites-manager-get-excluded-query-parameters.md) | GET |  |
| [SitesManager get Excluded Query Parameters Global](actions/sites-manager-get-excluded-query-parameters-global.md) | GET |  |
| [SitesManager get Excluded Referrers](actions/sites-manager-get-excluded-referrers.md) | GET |  |
| [SitesManager get Excluded Referrers Global](actions/sites-manager-get-excluded-referrers-global.md) | GET |  |
| [SitesManager get Excluded User Agents Global](actions/sites-manager-get-excluded-user-agents-global.md) | GET |  |
| [SitesManager get Exclusion Type For Query Params](actions/sites-manager-get-exclusion-type-for-query-params.md) | GET |  |
| [SitesManager get Image Tracking Code](actions/sites-manager-get-image-tracking-code.md) | GET |  |
| [SitesManager get Ips For Range](actions/sites-manager-get-ips-for-range.md) | GET |  |
| [SitesManager get Javascript Tag](actions/sites-manager-get-javascript-tag.md) | GET |  |
| [SitesManager get Keep URLFragments Global](actions/sites-manager-get-keep-url-fragments-global.md) | GET |  |
| [SitesManager get Num Websites To Display Per Page](actions/sites-manager-get-num-websites-to-display-per-page.md) | GET |  |
| [SitesManager get Pattern Match Sites](actions/sites-manager-get-pattern-match-sites.md) | GET |  |
| [SitesManager get Search Category Parameters Global](actions/sites-manager-get-search-category-parameters-global.md) | GET |  |
| [SitesManager get Search Keyword Parameters Global](actions/sites-manager-get-search-keyword-parameters-global.md) | GET |  |
| [SitesManager get Site From Id](actions/sites-manager-get-site-from-id.md) | GET |  |
| [SitesManager get Site Settings](actions/sites-manager-get-site-settings.md) | GET |  |
| [SitesManager get Site Urls From Id](actions/sites-manager-get-site-urls-from-id.md) | GET |  |
| [SitesManager get Sites From Group](actions/sites-manager-get-sites-from-group.md) | GET |  |
| [SitesManager get Sites Groups](actions/sites-manager-get-sites-groups.md) | GET |  |
| [SitesManager get Sites Id From Site Url](actions/sites-manager-get-sites-id-from-site-url.md) | GET |  |
| [SitesManager get Sites Id With Admin Access](actions/sites-manager-get-sites-id-with-admin-access.md) | GET |  |
| [SitesManager get Sites Id With At Least View Access](actions/sites-manager-get-sites-id-with-at-least-view-access.md) | GET |  |
| [SitesManager get Sites Id With View Access](actions/sites-manager-get-sites-id-with-view-access.md) | GET |  |
| [SitesManager get Sites Id With Write Access](actions/sites-manager-get-sites-id-with-write-access.md) | GET |  |
| [SitesManager get Sites With Admin Access](actions/sites-manager-get-sites-with-admin-access.md) | GET |  |
| [SitesManager get Sites With At Least View Access](actions/sites-manager-get-sites-with-at-least-view-access.md) | GET |  |
| [SitesManager get Sites With Minimum Access](actions/sites-manager-get-sites-with-minimum-access.md) | GET |  |
| [SitesManager get Sites With View Access](actions/sites-manager-get-sites-with-view-access.md) | GET |  |
| [SitesManager get Timezone Name](actions/sites-manager-get-timezone-name.md) | GET |  |
| [SitesManager get Timezones List](actions/sites-manager-get-timezones-list.md) | GET |  |
| [SitesManager get Unique Site Timezones](actions/sites-manager-get-unique-site-timezones.md) | GET |  |
| [SitesManager is Timezone Support Enabled](actions/sites-manager-is-timezone-support-enabled.md) | GET |  |
| [SitesManager rename Group](actions/sites-manager-rename-group.md) | GET |  |
| [SitesManager set Default Currency](actions/sites-manager-set-default-currency.md) | PUT |  |
| [SitesManager set Default Timezone](actions/sites-manager-set-default-timezone.md) | PUT |  |
| [SitesManager set Global Excluded Ips](actions/sites-manager-set-global-excluded-ips.md) | PUT |  |
| [SitesManager set Global Excluded Referrers](actions/sites-manager-set-global-excluded-referrers.md) | PUT |  |
| [SitesManager set Global Excluded User Agents](actions/sites-manager-set-global-excluded-user-agents.md) | PUT |  |
| [SitesManager set Global Query Param Exclusion](actions/sites-manager-set-global-query-param-exclusion.md) | PUT |  |
| [SitesManager set Global Search Parameters](actions/sites-manager-set-global-search-parameters.md) | PUT |  |
| [SitesManager set Keep URLFragments Global](actions/sites-manager-set-keep-url-fragments-global.md) | PUT |  |
| [SitesManager set Site Alias Urls](actions/sites-manager-set-site-alias-urls.md) | PUT |  |
| [SitesManager update Site](actions/sites-manager-update-site.md) | PUT |  |

### Tagmanager

| Action | Method | Description |
| --- | --- | --- |
| [TagManager add Container](actions/tag-manager-add-container.md) | POST |  |
| [TagManager add Container Tag](actions/tag-manager-add-container-tag.md) | POST |  |
| [TagManager add Container Trigger](actions/tag-manager-add-container-trigger.md) | POST |  |
| [TagManager add Container Variable](actions/tag-manager-add-container-variable.md) | POST |  |
| [TagManager change Debug Url](actions/tag-manager-change-debug-url.md) | GET |  |
| [TagManager create Container Version](actions/tag-manager-create-container-version.md) | POST |  |
| [TagManager create Default Container For Site](actions/tag-manager-create-default-container-for-site.md) | POST |  |
| [TagManager delete Container](actions/tag-manager-delete-container.md) | DELETE |  |
| [TagManager delete Container Tag](actions/tag-manager-delete-container-tag.md) | DELETE |  |
| [TagManager delete Container Trigger](actions/tag-manager-delete-container-trigger.md) | DELETE |  |
| [TagManager delete Container Variable](actions/tag-manager-delete-container-variable.md) | DELETE |  |
| [TagManager delete Container Version](actions/tag-manager-delete-container-version.md) | DELETE |  |
| [TagManager disable Preview Mode](actions/tag-manager-disable-preview-mode.md) | GET |  |
| [TagManager enable Preview Mode](actions/tag-manager-enable-preview-mode.md) | GET |  |
| [TagManager export Container Version](actions/tag-manager-export-container-version.md) | GET |  |
| [TagManager get Available Comparisons](actions/tag-manager-get-available-comparisons.md) | GET |  |
| [TagManager get Available Container Variables](actions/tag-manager-get-available-container-variables.md) | GET |  |
| [TagManager get Available Contexts](actions/tag-manager-get-available-contexts.md) | GET |  |
| [TagManager get Available Environments](actions/tag-manager-get-available-environments.md) | GET |  |
| [TagManager get Available Environments With Publish Capability](actions/tag-manager-get-available-environments-with-publish-capability.md) | GET |  |
| [TagManager get Available Tag Fire Limits](actions/tag-manager-get-available-tag-fire-limits.md) | GET |  |
| [TagManager get Available Tag Types In Context](actions/tag-manager-get-available-tag-types-in-context.md) | GET |  |
| [TagManager get Available Trigger Types In Context](actions/tag-manager-get-available-trigger-types-in-context.md) | GET |  |
| [TagManager get Available Variable Types In Context](actions/tag-manager-get-available-variable-types-in-context.md) | GET |  |
| [TagManager get Container](actions/tag-manager-get-container.md) | GET |  |
| [TagManager get Container Embed Code](actions/tag-manager-get-container-embed-code.md) | GET |  |
| [TagManager get Container Install Instructions](actions/tag-manager-get-container-install-instructions.md) | GET |  |
| [TagManager get Container Tag](actions/tag-manager-get-container-tag.md) | GET |  |
| [TagManager get Container Tags](actions/tag-manager-get-container-tags.md) | GET |  |
| [TagManager get Container Trigger](actions/tag-manager-get-container-trigger.md) | GET |  |
| [TagManager get Container Trigger References](actions/tag-manager-get-container-trigger-references.md) | GET |  |
| [TagManager get Container Triggers](actions/tag-manager-get-container-triggers.md) | GET |  |
| [TagManager get Container Variable](actions/tag-manager-get-container-variable.md) | GET |  |
| [TagManager get Container Variable References](actions/tag-manager-get-container-variable-references.md) | GET |  |
| [TagManager get Container Variables](actions/tag-manager-get-container-variables.md) | GET |  |
| [TagManager get Container Version](actions/tag-manager-get-container-version.md) | GET |  |
| [TagManager get Container Versions](actions/tag-manager-get-container-versions.md) | GET |  |
| [TagManager get Containers](actions/tag-manager-get-containers.md) | GET |  |
| [TagManager import Container Version](actions/tag-manager-import-container-version.md) | GET |  |
| [TagManager pause Container Tag](actions/tag-manager-pause-container-tag.md) | PUT |  |
| [TagManager publish Container Version](actions/tag-manager-publish-container-version.md) | GET |  |
| [TagManager resume Container Tag](actions/tag-manager-resume-container-tag.md) | PUT |  |
| [TagManager update Container](actions/tag-manager-update-container.md) | PUT |  |
| [TagManager update Container Tag](actions/tag-manager-update-container-tag.md) | PUT |  |
| [TagManager update Container Trigger](actions/tag-manager-update-container-trigger.md) | PUT |  |
| [TagManager update Container Variable](actions/tag-manager-update-container-variable.md) | PUT |  |
| [TagManager update Container Version](actions/tag-manager-update-container-version.md) | PUT |  |

### Tour

| Action | Method | Description |
| --- | --- | --- |
| [Tour get Challenges](actions/tour-get-challenges.md) | GET |  |
| [Tour get Level](actions/tour-get-level.md) | GET |  |
| [Tour skip Challenge](actions/tour-skip-challenge.md) | GET |  |

### Transitions

| Action | Method | Description |
| --- | --- | --- |
| [Transitions get Transitions For Action](actions/transitions-get-transitions-for-action.md) | GET |  |
| [Transitions get Transitions For Page Title](actions/transitions-get-transitions-for-page-title.md) | GET |  |
| [Transitions get Transitions For Page Url](actions/transitions-get-transitions-for-page-url.md) | GET |  |
| [Transitions get Translations](actions/transitions-get-translations.md) | GET |  |
| [Transitions is Period Allowed](actions/transitions-is-period-allowed.md) | GET |  |

### Twofactorauth

| Action | Method | Description |
| --- | --- | --- |
| [TwoFactorAuth reset Two Factor Auth](actions/two-factor-auth-reset-two-factor-auth.md) | GET |  |

### Usercountry

| Action | Method | Description |
| --- | --- | --- |
| [UserCountry get Country Code Mapping](actions/user-country-get-country-code-mapping.md) | GET |  |
| [UserCountry get Location From IP](actions/user-country-get-location-from-ip.md) | GET |  |
| [UserCountry get Number Of Distinct Countries](actions/user-country-get-number-of-distinct-countries.md) | GET |  |
| [UserCountry set Location Provider](actions/user-country-set-location-provider.md) | PUT |  |

### Usersflow

| Action | Method | Description |
| --- | --- | --- |
| [UsersFlow get Available Data Sources](actions/users-flow-get-available-data-sources.md) | GET |  |
| [UsersFlow get Interaction Actions](actions/users-flow-get-interaction-actions.md) | GET |  |
| [UsersFlow get Users Flow](actions/users-flow-get-users-flow.md) | GET |  |

### Usersmanager

| Action | Method | Description |
| --- | --- | --- |
| [UsersManager add Capabilities](actions/users-manager-add-capabilities.md) | POST |  |
| [UsersManager add User](actions/users-manager-add-user.md) | POST |  |
| [UsersManager create App Specific Token Auth](actions/users-manager-create-app-specific-token-auth.md) | POST |  |
| [UsersManager delete User](actions/users-manager-delete-user.md) | DELETE |  |
| [UsersManager generate Invite Link](actions/users-manager-generate-invite-link.md) | GET |  |
| [UsersManager get Available Capabilities](actions/users-manager-get-available-capabilities.md) | GET |  |
| [UsersManager get Available Roles](actions/users-manager-get-available-roles.md) | GET |  |
| [UsersManager get Sites Access For User](actions/users-manager-get-sites-access-for-user.md) | GET |  |
| [UsersManager get Sites Access From User](actions/users-manager-get-sites-access-from-user.md) | GET |  |
| [UsersManager get User](actions/users-manager-get-user.md) | GET |  |
| [UsersManager get User By Email](actions/users-manager-get-user-by-email.md) | GET |  |
| [UsersManager get User Login From User Email](actions/users-manager-get-user-login-from-user-email.md) | GET |  |
| [UsersManager get User Preference](actions/users-manager-get-user-preference.md) | GET |  |
| [UsersManager get Users](actions/users-manager-get-users.md) | GET |  |
| [UsersManager get Users Access From Site](actions/users-manager-get-users-access-from-site.md) | GET |  |
| [UsersManager get Users Having Super User Access](actions/users-manager-get-users-having-super-user-access.md) | GET |  |
| [UsersManager get Users Login](actions/users-manager-get-users-login.md) | GET |  |
| [UsersManager get Users Plus Role](actions/users-manager-get-users-plus-role.md) | GET |  |
| [UsersManager get Users Sites From Access](actions/users-manager-get-users-sites-from-access.md) | GET |  |
| [UsersManager get Users With Site Access](actions/users-manager-get-users-with-site-access.md) | GET |  |
| [UsersManager has Super User Access](actions/users-manager-has-super-user-access.md) | GET |  |
| [UsersManager invite User](actions/users-manager-invite-user.md) | GET |  |
| [UsersManager logout User](actions/users-manager-logout-user.md) | GET |  |
| [UsersManager newsletter Signup](actions/users-manager-newsletter-signup.md) | GET |  |
| [UsersManager remove Capabilities](actions/users-manager-remove-capabilities.md) | DELETE |  |
| [UsersManager resend Invite](actions/users-manager-resend-invite.md) | GET |  |
| [UsersManager set Super User Access](actions/users-manager-set-super-user-access.md) | PUT |  |
| [UsersManager set User Access](actions/users-manager-set-user-access.md) | PUT |  |
| [UsersManager set User Preference](actions/users-manager-set-user-preference.md) | PUT |  |
| [UsersManager update User](actions/users-manager-update-user.md) | PUT |  |
| [UsersManager user Email Exists](actions/users-manager-user-email-exists.md) | GET |  |
| [UsersManager user Exists](actions/users-manager-user-exists.md) | GET |  |

### Visitssummary

| Action | Method | Description |
| --- | --- | --- |
| [VisitsSummary get Actions](actions/visits-summary-get-actions.md) | GET |  |
| [VisitsSummary get Bounce Count](actions/visits-summary-get-bounce-count.md) | GET |  |
| [VisitsSummary get Max Actions](actions/visits-summary-get-max-actions.md) | GET |  |
| [VisitsSummary get Sum Visits Length](actions/visits-summary-get-sum-visits-length.md) | GET |  |
| [VisitsSummary get Sum Visits Length Pretty](actions/visits-summary-get-sum-visits-length-pretty.md) | GET |  |
| [VisitsSummary get Unique Visitors](actions/visits-summary-get-unique-visitors.md) | GET |  |
| [VisitsSummary get Users](actions/visits-summary-get-users.md) | GET |  |
| [VisitsSummary get Visits](actions/visits-summary-get-visits.md) | GET |  |
| [VisitsSummary get Visits Converted](actions/visits-summary-get-visits-converted.md) | GET |  |

