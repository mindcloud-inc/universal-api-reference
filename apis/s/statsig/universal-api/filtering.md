# Statsig Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Statsig expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Statsig actions that support filtering

- [Delete Ingestion Source](actions/delete-ingestion-source-delete-console-v1-ingestion.md)
- [Fully Update Dynamic Config](actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id.md)
- [Get Ingestion Event Count](actions/get-ingestion-event-count-get-console-v1-ingestion-events-count.md)
- [Get Ingestion Event Delta Ledger](actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta.md)
- [Get Report in CSV format](actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report.md)
- [Get Reports](actions/get-reports-get-console-v1-reports.md)
- [Lineage: List experiments related to Metric](actions/lineage-list-experiments-related-to-metric-get-console-v1-metrics-id-experiments.md)
- [List All Metric Values](actions/list-all-metric-values-get-console-v1-metrics-values.md)
- [List all Metrics](actions/list-all-metrics-get-console-v1-metrics-list.md)
- [List Audit Logs](actions/list-audit-logs-get-console-v1-audit-logs.md)
- [List Dashboards](actions/list-dashboards-get-console-v1-dashboards.md)
- [List Dynamic Configs](actions/list-dynamic-configs-get-console-v1-dynamic-configs.md)
- [List Experiments](actions/list-experiments-get-console-v1-experiments.md)
- [List Gates](actions/list-gates-get-console-v1-gates.md)
- [List Holdouts](actions/list-holdouts-get-console-v1-holdouts.md)
- [List Ingestions Status](actions/list-ingestions-status-get-console-v1-ingestion-status.md)
- [List Keys](actions/list-keys-get-console-v1-keys.md)
- [List Pipeline Triggers](actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers.md)
- [List Users](actions/list-users-get-console-v1-users.md)
- [Load Pulse (Warehouse Native)](actions/load-pulse-warehouse-native-post-console-v1-experiments-id-load-pulse.md)
- [Partially Update Dynamic Config](actions/partially-update-dynamic-config-patch-console-v1-dynamic-configs-id.md)
- [Read Dashboard Widget Results](actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results.md)
- [Read Exposure Event Count](actions/read-exposure-event-count-get-console-v1-exposure-count.md)
- [Read Ingestion](actions/read-ingestion-get-console-v1-ingestion.md)
- [Read Ingestion Schedule](actions/read-ingestion-schedule-get-console-v1-ingestion-schedule.md)
- [Read Single Metric Value](actions/read-single-metric-value-get-console-v1-metrics.md)
- [Reload metric data](actions/reload-metric-data-post-console-v1-metrics-id-reload.md)
- [Retrieve Experiment Checks Diagnostics](actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks.md)
- [Retrieve Experiment Summary Charts (Beta)](actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts.md)
- [Retrieve Exposures By Dimension](actions/retrieve-exposures-by-dimension-get-console-v1-experiments-id-dimensional-exposures.md)
- [Retrieve Pulse Metric Result](actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result.md)
- [Retrieve Pulse Results (Beta)](actions/retrieve-pulse-results-beta-get-console-v1-experiments-id-pulse-results.md)
- [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results.md)
- [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-holdouts-id-pulse-results.md)
- [Update Dynamic Config Rule By Id](actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid.md)
