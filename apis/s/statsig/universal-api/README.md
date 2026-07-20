# <img src="https://images.mindcloud.co/apps/icons/statsig-icon_1776713640905.png" alt="Statsig logo" width="28" height="28"> Statsig: Universal API

Statsig Console API integration for managing feature gates, experiments, configs, metrics, segments, keys, environments, users, and other project resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/statsig/latest
- **Actions:** 279
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.statsig.com
- **Vendor API docs:** https://docs.statsig.com/console-api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Info](actions/get-company-info-get-console-v1-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (279)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Topline Alert Events](actions/list-topline-alert-events-get-console-v1-alerts-id-events.md) | GET | Retrieves topline alert events from Statsig. |
| [List Topline Alerts](actions/list-topline-alerts-get-console-v1-alerts.md) | GET | Retrieves topline alerts from Statsig. |
| [Read Topline Alert Event](actions/read-topline-alert-event-get-console-v1-alerts-id-events-eventid.md) | GET | Retrieves a topline alert event from Statsig. |
| [Read Topline Alert](actions/read-topline-alert-get-console-v1-alerts-id.md) | GET | Retrieves a topline alert from Statsig. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs-get-console-v1-audit-logs.md) | GET | Retrieves audit logs from Statsig. |

### Autotune

| Action | Method | Description |
| --- | --- | --- |
| [Get Ranked List for Contextual Bandit](actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list.md) | GET | Retrieves a ranked list from Statsig for contextual bandits. |

### Autotunes

| Action | Method | Description |
| --- | --- | --- |
| [Create Autotune](actions/create-autotune-post-console-v1-autotunes.md) | POST | Creates an autotune in Statsig. |
| [Delete Autotune](actions/delete-autotune-delete-console-v1-autotunes-id.md) | DELETE | Deletes an autotune from Statsig. |
| [Finish Experiment Early](actions/finish-experiment-early-put-console-v1-autotunes-id-make-decision.md) | PUT | Finishes an experiment early in Statsig. |
| [Fully Update Autotune](actions/fully-update-autotune-post-console-v1-autotunes-id.md) | PUT | Updates an autotune in Statsig. |
| [List Autotune](actions/list-autotune-get-console-v1-autotunes.md) | GET | Retrieves autotunes from Statsig. |
| [Partially Update Autotune](actions/partially-update-autotune-patch-console-v1-autotunes-id.md) | PUT | Updates an autotune in Statsig. |
| [Read Autotune](actions/read-autotune-get-console-v1-autotunes-id.md) | GET | Retrieves an autotune from Statsig. |
| [Reset Experiment](actions/reset-experiment-put-console-v1-autotunes-id-reset.md) | PUT | Resets an experiment in Statsig. |
| [Start Autotune Experiment](actions/start-autotune-experiment-put-console-v1-autotunes-id-start.md) | PUT | Starts an autotune experiment in Statsig. |

### Change Validation

| Action | Method | Description |
| --- | --- | --- |
| [Change Validation](actions/change-validation-post-console-v1-change-validation.md) | POST | Creates a change validation in Statsig. |
| [Update change validation message](actions/update-change-validation-message-patch-console-v1-change-validation-message.md) | PUT | Updates a change validation message in Statsig. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info-get-console-v1-company.md) | GET | Retrieves company info from Statsig. |

### Configs

| Action | Method | Description |
| --- | --- | --- |
| [Read Exposure Event Count](actions/read-exposure-event-count-get-console-v1-exposure-count.md) | GET | Retrieves exposure event counts from Statsig. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Add Widgets to Dashboard](actions/add-widgets-to-dashboard-post-console-v1-dashboards-id-widgets.md) | POST | Adds widgets to dashboard in Statsig. |
| [Create Dashboard](actions/create-dashboard-post-console-v1-dashboards.md) | POST | Creates a dashboard in Statsig. |
| [List Dashboards](actions/list-dashboards-get-console-v1-dashboards.md) | GET | Retrieves dashboards from Statsig. |
| [Read Dashboard](actions/read-dashboard-get-console-v1-dashboards-id.md) | GET | Retrieves a dashboard from Statsig. |
| [Read Dashboard Widget Results](actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results.md) | GET | Retrieves dashboard widget results from Statsig. |
| [Replace Widgets on Dashboard](actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets.md) | GET | Replaces widgets on dashboard in Statsig. |

### Dynamic Configs

| Action | Method | Description |
| --- | --- | --- |
| [Archive Dynamic Config](actions/archive-dynamic-config-put-console-v1-dynamic-configs-id-archive.md) | DELETE | Archives a dynamic config in Statsig. |
| [Commit Dynamic Config Review](actions/commit-dynamic-config-review-put-console-v1-dynamic-configs-id-reviews-reviewid-commit.md) | PUT | Commits a dynamic config review in Statsig. |
| [Create Dynamic Config](actions/create-dynamic-config-post-console-v1-dynamic-configs.md) | POST | Creates a dynamic config in Statsig. |
| [Delete Dynamic Config](actions/delete-dynamic-config-delete-console-v1-dynamic-configs-id.md) | DELETE | Deletes a dynamic config from Statsig. |
| [Delete Dynamic Config Rule](actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid.md) | DELETE | Deletes a dynamic config rule from Statsig. |
| [Disable Dynamic Config](actions/disable-dynamic-config-put-console-v1-dynamic-configs-id-disable.md) | PUT | Disables a dynamic config in Statsig. |
| [Enable Dynamic Config](actions/enable-dynamic-config-put-console-v1-dynamic-configs-id-enable.md) | PUT | Enables a dynamic config in Statsig. |
| [Fully Update Dynamic Config](actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id.md) | PUT | Updates a dynamic config in Statsig. |
| [Get Dynamic Config](actions/get-dynamic-config-get-console-v1-dynamic-configs-id.md) | GET | Retrieves a dynamic config from Statsig. |
| [Get Dynamic Config or Experiment](actions/get-dynamic-config-or-experiment-post-v1-get-config.md) | GET | Retrieves a dynamic config or experiment from Statsig. |
| [Get Dynamic Config Rules](actions/get-dynamic-config-rules-get-console-v1-dynamic-configs-id-rules.md) | GET | Retrieves dynamic config rules from Statsig. |
| [Get Specific Dynamic Config Rule](actions/get-specific-dynamic-config-rule-get-console-v1-dynamic-configs-id-rule-ruleid.md) | GET | Retrieves a specific dynamic config rule from Statsig. |
| [List Dynamic Config Versions](actions/list-dynamic-config-versions-get-console-v1-dynamic-configs-id-versions.md) | GET | Retrieves dynamic config versions from Statsig. |
| [List Dynamic Configs](actions/list-dynamic-configs-get-console-v1-dynamic-configs.md) | GET | Retrieves dynamic configs from Statsig. |
| [Partially Update Dynamic Config](actions/partially-update-dynamic-config-patch-console-v1-dynamic-configs-id.md) | PUT | Updates a dynamic config in Statsig. |
| [Unarchive Dynamic Config](actions/unarchive-dynamic-config-put-console-v1-dynamic-configs-id-unarchive.md) | PUT | Unarchives a dynamic config in Statsig. |
| [Update Dynamic Config Rule By Id](actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid.md) | PUT | Updates a dynamic config rule in Statsig. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Get Environments](actions/get-environments-get-console-v1-environments.md) | GET | Retrieves environments from Statsig. |
| [Update Environments](actions/update-environments-post-console-v1-environments.md) | PUT | Updates environments in Statsig. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get metrics using event name](actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics.md) | GET | Retrieves metrics from Statsig by event name. |
| [Get specific events](actions/get-specific-events-get-console-v1-events-eventname.md) | GET | Retrieves a specific event from Statsig. |
| [List Events](actions/list-events-get-console-v1-events.md) | GET | Retrieves events from Statsig. |
| [Log Custom Events](actions/log-custom-events-post-v1-log-event.md) | POST | Logs custom events to Statsig. |
| [Log Custom Exposure Events](actions/log-custom-exposure-events-post-v1-log-custom-exposure.md) | POST | Logs custom exposure events to Statsig. |

### Experiments

| Action | Method | Description |
| --- | --- | --- |
| [Abandon Experiment](actions/abandon-experiment-put-console-v1-experiments-id-abandon.md) | PUT | Abandons an experiment in Statsig. |
| [Archive Experiment](actions/archive-experiment-put-console-v1-experiments-id-archive.md) | DELETE | Archives an experiment in Statsig. |
| [Cancel Pulse Load (Warehouse Native)](actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid.md) | POST | Cancels a warehouse-native pulse load in Statsig. |
| [Commit Experiment Review](actions/commit-experiment-review-put-console-v1-experiments-id-reviews-reviewid-commit.md) | PUT | Commits an experiment review in Statsig. |
| [Conclude Experiment & Defer Decision](actions/conclude-experiment-defer-decision-put-console-v1-experiments-id-defer-decision.md) | PUT | Concludes an experiment and defers its decision in Statsig. |
| [Create Assignment Source](actions/create-assignment-source-post-console-v1-experiments-assignment-sources.md) | POST | Creates an assignment source in Statsig. |
| [Create Entity Property Source](actions/create-entity-property-source-post-console-v1-experiments-entity-properties.md) | POST | Creates an entity property source in Statsig. |
| [Create Experiment](actions/create-experiment-post-console-v1-experiments.md) | POST | Creates an experiment in Statsig. |
| [Delete Assignment Source](actions/delete-assignment-source-delete-console-v1-experiments-assignment-source-name.md) | DELETE | Deletes an assignment source from Statsig. |
| [Delete Entity Property Source](actions/delete-entity-property-source-delete-console-v1-experiments-entity-property-name.md) | DELETE | Deletes an entity property source from Statsig. |
| [Delete Experiment Overrides](actions/delete-experiment-overrides-delete-console-v1-experiments-id-overrides.md) | DELETE | Deletes experiment overrides from Statsig. |
| [Deleted Experiment](actions/deleted-experiment-delete-console-v1-experiments-id.md) | DELETE | Deletes an experiment from Statsig. |
| [Disable Experiment Groups](actions/disable-experiment-groups-post-console-v1-experiments-id-disable-groups.md) | PUT | Disables experiment groups in Statsig. |
| [Enable Experiment Groups](actions/enable-experiment-groups-post-console-v1-experiments-id-enable-groups.md) | PUT | Enables experiment groups in Statsig. |
| [Finish Experiment Early](actions/finish-experiment-early-put-console-v1-experiments-id-make-decision.md) | PUT | Finishes an experiment early in Statsig. |
| [Fully Update Experiment](actions/fully-update-experiment-post-console-v1-experiments-id.md) | PUT | Updates an experiment in Statsig. |
| [Get Entity Property Source](actions/get-entity-property-source-get-console-v1-experiments-entity-property-name.md) | GET | Retrieves an entity property source from Statsig. |
| [Get Experiment Context](actions/get-experiment-context-get-console-v1-experiments-id-context.md) | GET | Retrieves experiment context from Statsig. |
| [Get Experiment](actions/get-experiment-get-console-v1-experiments-id.md) | GET | Retrieves an experiment from Statsig. |
| [Get Experiment Guardrail Alert Statuses](actions/get-experiment-guardrail-alert-statuses-get-console-v1-experiments-id-alerts.md) | GET | Retrieves experiment guardrail alert statuses from Statsig. |
| [Get Experiment Overrides](actions/get-experiment-overrides-get-console-v1-experiments-id-overrides.md) | GET | Retrieves experiment overrides from Statsig. |
| [Get Pulse Load History Details (Warehouse Native)](actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h.md) | GET | Retrieves warehouse-native pulse load history details from Statsig. |
| [List Assignment Sources](actions/list-assignment-sources-get-console-v1-experiments-assignment-sources.md) | GET | Retrieves assignment sources from Statsig. |
| [List Entity Property Sources](actions/list-entity-property-sources-get-console-v1-experiments-entity-properties.md) | GET | Retrieves entity property sources from Statsig. |
| [List Experiment Versions](actions/list-experiment-versions-get-console-v1-experiments-id-versions.md) | GET | Retrieves experiment versions from Statsig. |
| [List Experiments](actions/list-experiments-get-console-v1-experiments.md) | GET | Retrieves experiments from Statsig. |
| [Load Pulse (Warehouse Native)](actions/load-pulse-warehouse-native-post-console-v1-experiments-id-load-pulse.md) | POST | Loads a warehouse-native pulse in Statsig. |
| [Partially Update Experiment Overrides](actions/partially-update-experiment-overrides-patch-console-v1-experiments-id-overrides.md) | PUT | Updates experiment overrides in Statsig. |
| [Partially Update Experiment](actions/partially-update-experiment-patch-console-v1-experiments-id.md) | PUT | Updates an experiment in Statsig. |
| [Patch Assignment Source](actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name.md) | PUT | Updates an assignment source in Statsig. |
| [Patch Entity Property Source](actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name.md) | PUT | Updates an entity property source in Statsig. |
| [Post Assignment Source](actions/post-assignment-source-post-console-v1-experiments-assignment-source-name.md) | POST | Creates an assignment source in Statsig. |
| [Post Entity Property Source](actions/post-entity-property-source-post-console-v1-experiments-entity-property-name.md) | POST | Creates an entity property source in Statsig. |
| [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-experiments-id-pulse-load-history.md) | GET | Retrieves warehouse-native pulse load history from Statsig. |
| [Reset Experiment](actions/reset-experiment-put-console-v1-experiments-id-reset.md) | PUT | Resets an experiment in Statsig. |
| [Resolve Metric Rollout Alert](actions/resolve-metric-rollout-alert-post-console-v1-experiments-id-alerts-metricid-resolve.md) | POST | Resolves a metric rollout alert in Statsig. |
| [Restart As New Experiment](actions/restart-as-new-experiment-post-console-v1-experiments-id-restart-as-new.md) | PUT | Restarts an experiment as new in Statsig. |
| [Retrieve cumulative exposures](actions/retrieve-cumulative-exposures-get-console-v1-experiments-id-cumulative-exposures.md) | GET | Retrieves cumulative exposures from Statsig. |
| [Retrieve Experiment Checks Diagnostics](actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks.md) | GET | Retrieves experiment checks diagnostics from Statsig. |
| [Retrieve Experiment Summary Charts (Beta)](actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts.md) | GET | Retrieves experiment summary charts from Statsig. |
| [Retrieve Exposures By Dimension](actions/retrieve-exposures-by-dimension-get-console-v1-experiments-id-dimensional-exposures.md) | GET | Retrieves exposures by dimension from Statsig. |
| [Retrieve Pulse Metric Result](actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result.md) | GET | Retrieves a pulse metric result from Statsig. |
| [Retrieve Pulse Results (Beta)](actions/retrieve-pulse-results-beta-get-console-v1-experiments-id-pulse-results.md) | GET | Retrieves pulse results from Statsig. |
| [Schedule Experiment Start](actions/schedule-experiment-start-post-console-v1-experiments-id-schedule-start.md) | PUT | Schedules an experiment start in Statsig. |
| [Start Experiment Code Cleanup](actions/start-experiment-code-cleanup-post-console-v1-experiments-id-code-cleanup.md) | PUT | Starts experiment code cleanup in Statsig. |
| [Start Experiment](actions/start-experiment-put-console-v1-experiments-id-start.md) | PUT | Starts an experiment in Statsig. |
| [Unarchive Experiment](actions/unarchive-experiment-put-console-v1-experiments-id-unarchive.md) | PUT | Unarchives an experiment in Statsig. |
| [Update Experiment Overrides](actions/update-experiment-overrides-post-console-v1-experiments-id-overrides.md) | PUT | Updates experiment overrides in Statsig. |

### Experiments (warehouse Native)

| Action | Method | Description |
| --- | --- | --- |
| [Create Qualifying Event](actions/create-qualifying-event-post-console-v1-experiments-qualifying-events.md) | POST | Creates a qualifying event in Statsig. |
| [Delete Qualifying Event](actions/delete-qualifying-event-delete-console-v1-experiments-qualifying-events-name.md) | DELETE | Deletes a qualifying event from Statsig. |
| [List qualifying event](actions/list-qualifying-event-get-console-v1-experiments-qualifying-events.md) | GET | Retrieves qualifying events from Statsig. |
| [Read Qualifying Event](actions/read-qualifying-event-get-console-v1-experiments-qualifying-events-name.md) | GET | Retrieves a qualifying event from Statsig. |
| [Update Qualifying Event](actions/update-qualifying-event-post-console-v1-experiments-qualifying-events-name.md) | PUT | Updates a qualifying event in Statsig. |

### Feature Gates

| Action | Method | Description |
| --- | --- | --- |
| [Check Feature Gates](actions/check-feature-gates-post-v1-check-gate.md) | GET | Checks feature gates in Statsig. |

### Gates

| Action | Method | Description |
| --- | --- | --- |
| [Add Gate Overrides](actions/add-gate-overrides-patch-console-v1-gates-id-overrides.md) | POST | Adds gate overrides in Statsig. |
| [Add Gate Rule](actions/add-gate-rule-post-console-v1-gates-id-rule.md) | POST | Adds gate rule in Statsig. |
| [Archive Gate](actions/archive-gate-put-console-v1-gates-id-archive.md) | DELETE | Archives a gate in Statsig. |
| [Commit Gate Review](actions/commit-gate-review-put-console-v1-gates-id-reviews-reviewid-commit.md) | PUT | Commits a gate review in Statsig. |
| [Create Gate](actions/create-gate-post-console-v1-gates.md) | POST | Creates a gate in Statsig. |
| [Delete Gate Overrides](actions/delete-gate-overrides-delete-console-v1-gates-id-overrides.md) | DELETE | Deletes gate overrides from Statsig. |
| [Delete Gate Rule](actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid.md) | DELETE | Deletes a gate rule from Statsig. |
| [Delete Gates](actions/delete-gates-delete-console-v1-gates-id.md) | DELETE | Deletes gates from Statsig. |
| [Disable Gate](actions/disable-gate-put-console-v1-gates-id-disable.md) | PUT | Disables a gate in Statsig. |
| [Enable Gate](actions/enable-gate-put-console-v1-gates-id-enable.md) | PUT | Enables a gate in Statsig. |
| [Fully Update Gates](actions/fully-update-gates-post-console-v1-gates-id.md) | PUT | Updates gates in Statsig. |
| [Get Gate Override](actions/get-gate-override-get-console-v1-gates-id-overrides.md) | GET | Retrieves a gate override from Statsig. |
| [Launch Gate](actions/launch-gate-put-console-v1-gates-id-launch.md) | PUT | Launches a gate in Statsig. |
| [List Dynamic Config References](actions/list-dynamic-config-references-get-console-v1-gates-id-dynamic-config-references.md) | GET | Retrieves dynamic config references from Statsig. |
| [List Experiment References](actions/list-experiment-references-get-console-v1-gates-id-experiment-references.md) | GET | Retrieves experiment references from Statsig. |
| [List Gate References](actions/list-gate-references-get-console-v1-gates-id-gate-references.md) | GET | Retrieves gate references from Statsig. |
| [List Gate Versions](actions/list-gate-versions-get-console-v1-gates-id-versions.md) | GET | Retrieves gate versions from Statsig. |
| [List Gates](actions/list-gates-get-console-v1-gates.md) | GET | Retrieves gates from Statsig. |
| [Load Pulse Gate](actions/load-pulse-gate-post-console-v1-gates-id-load-pulse.md) | POST | Loads a pulse gate in Statsig. |
| [Partially Update Gates](actions/partially-update-gates-patch-console-v1-gates-id.md) | PUT | Updates gates in Statsig. |
| [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-gates-id-rules-ruleid-pulse-load-histor.md) | GET | Retrieves warehouse-native pulse load history from Statsig. |
| [Read Gate Checks](actions/read-gate-checks-get-console-v1-gates-id-checks.md) | GET | Retrieves gate checks from Statsig. |
| [Read Gate](actions/read-gate-get-console-v1-gates-id.md) | GET | Retrieves a gate from Statsig. |
| [Read Gate Rules](actions/read-gate-rules-get-console-v1-gates-id-rules.md) | GET | Retrieves gate rules from Statsig. |
| [Resolve Metric Rollout Alert](actions/resolve-metric-rollout-alert-post-console-v1-gates-id-alerts-metricid-resolve.md) | POST | Resolves a metric rollout alert in Statsig. |
| [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results.md) | GET | Retrieves pulse results from Statsig. |
| [Start Gate Code Cleanup](actions/start-gate-code-cleanup-post-console-v1-gates-id-code-cleanup.md) | PUT | Starts gate code cleanup in Statsig. |
| [Unarchive Gate](actions/unarchive-gate-put-console-v1-gates-id-unarchive.md) | PUT | Unarchives a gate in Statsig. |
| [Update Gate Overrides](actions/update-gate-overrides-post-console-v1-gates-id-overrides.md) | PUT | Updates gate overrides in Statsig. |
| [Update Gate Rules](actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid.md) | PUT | Updates gate rules in Statsig. |

### Holdouts

| Action | Method | Description |
| --- | --- | --- |
| [Add Holdout Overrides](actions/add-holdout-overrides-patch-console-v1-holdouts-id-overrides.md) | POST | Adds holdout overrides in Statsig. |
| [Create holdout](actions/create-holdout-post-console-v1-holdouts.md) | POST | Creates a holdout in Statsig. |
| [Delete holdout by id](actions/delete-holdout-by-id-delete-console-v1-holdouts-id.md) | DELETE | Deletes a holdout from Statsig by ID. |
| [Get holdout by id](actions/get-holdout-by-id-get-console-v1-holdouts-id.md) | GET | Retrieves a holdout from Statsig by ID. |
| [List Holdouts](actions/list-holdouts-get-console-v1-holdouts.md) | GET | Retrieves holdouts from Statsig. |
| [Partially update holdout by id](actions/partially-update-holdout-by-id-patch-console-v1-holdouts-id.md) | PUT | Updates a holdout in Statsig by ID. |
| [Read Holdout Overrides](actions/read-holdout-overrides-get-console-v1-holdouts-id-overrides.md) | GET | Retrieves holdout overrides from Statsig. |
| [Remove Holdout Overrides](actions/remove-holdout-overrides-delete-console-v1-holdouts-id-overrides.md) | DELETE | Removes holdout overrides in Statsig. |
| [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-holdouts-id-pulse-results.md) | GET | Retrieves pulse results from Statsig. |
| [Update holdout by id](actions/update-holdout-by-id-post-console-v1-holdouts-id.md) | PUT | Updates a holdout in Statsig by ID. |
| [Update Holdout Overrides](actions/update-holdout-overrides-post-console-v1-holdouts-id-overrides.md) | PUT | Updates holdout overrides in Statsig. |

### Ingestions

| Action | Method | Description |
| --- | --- | --- |
| [Backfill Ingestion](actions/backfill-ingestion-post-console-v1-ingestion-backfill.md) | POST | Backfills an ingestion in Statsig. |
| [Create Ingestion Databricks](actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks.md) | POST | Creates a Databricks ingestion in Statsig. |
| [Create Ingestion Source](actions/create-ingestion-source-post-console-v1-ingestion.md) | POST | Creates an ingestion source in Statsig. |
| [Delete Ingestion Source](actions/delete-ingestion-source-delete-console-v1-ingestion.md) | DELETE | Deletes an ingestion source from Statsig. |
| [Get Ingestion Event Count](actions/get-ingestion-event-count-get-console-v1-ingestion-events-count.md) | GET | Retrieves an ingestion event count from Statsig. |
| [Get Ingestion Event Delta Ledger](actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta.md) | GET | Retrieves an ingestion event delta ledger from Statsig. |
| [List Ingestion Runs](actions/list-ingestion-runs-get-console-v1-ingestion-runs.md) | GET | Retrieves ingestion runs from Statsig. |
| [List Ingestions Status](actions/list-ingestions-status-get-console-v1-ingestion-status.md) | GET | Retrieves ingestion statuses from Statsig. |
| [Read Ingestion](actions/read-ingestion-get-console-v1-ingestion.md) | GET | Retrieves an ingestion from Statsig. |
| [Read Ingestion Run](actions/read-ingestion-run-get-console-v1-ingestion-runs-id.md) | GET | Retrieves an ingestion run from Statsig. |
| [Read Ingestion Schedule](actions/read-ingestion-schedule-get-console-v1-ingestion-schedule.md) | GET | Retrieves an ingestion schedule from Statsig. |
| [Update Ingestion Schedule](actions/update-ingestion-schedule-post-console-v1-ingestion-schedule.md) | PUT | Updates an ingestion schedule in Statsig. |
| [Update Ingestion Source](actions/update-ingestion-source-patch-console-v1-ingestion.md) | PUT | Updates an ingestion source in Statsig. |

### Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create Key](actions/create-key-post-console-v1-keys.md) | POST | Creates a key in Statsig. |
| [Deactivate Key](actions/deactivate-key-patch-console-v1-keys-id-deactivate.md) | DELETE | Deactivates a key in Statsig. |
| [Delete Key](actions/delete-key-delete-console-v1-keys-id.md) | DELETE | Deletes a key from Statsig. |
| [List Keys](actions/list-keys-get-console-v1-keys.md) | GET | Retrieves keys from Statsig. |
| [Read Key](actions/read-key-get-console-v1-keys-id.md) | GET | Retrieves a key from Statsig. |
| [Rotate Key](actions/rotate-key-patch-console-v1-keys-id-rotate.md) | PUT | Rotates a key in Statsig. |
| [Update Key](actions/update-key-patch-console-v1-keys-id.md) | PUT | Updates a key in Statsig. |

### Layers

| Action | Method | Description |
| --- | --- | --- |
| [Add Layer Overrides](actions/add-layer-overrides-patch-console-v1-layers-id-overrides.md) | POST | Adds layer overrides in Statsig. |
| [Create a Layer](actions/create-a-layer-post-console-v1-layers.md) | POST | Creates a layer in Statsig. |
| [Delete a layer](actions/delete-a-layer-delete-console-v1-layers-id.md) | DELETE | Deletes a layer from Statsig. |
| [Delete Layer Overrides](actions/delete-layer-overrides-delete-console-v1-layers-id-overrides.md) | DELETE | Deletes layer overrides from Statsig. |
| [Get Layer Overrides](actions/get-layer-overrides-get-console-v1-layers-id-overrides.md) | GET | Retrieves layer overrides from Statsig. |
| [Get Layer Parameters](actions/get-layer-parameters-post-v1-get-layer.md) | GET | Retrieves layer parameters from Statsig. |
| [Get Layers](actions/get-layers-get-console-v1-layers.md) | GET | Retrieves layers from Statsig. |
| [Get one layer](actions/get-one-layer-get-console-v1-layers-id.md) | GET | Retrieves a layer from Statsig. |
| [Lineage: List Experiment related to Layer](actions/lineage-list-experiment-related-to-layer-get-console-v1-layers-id-experiments.md) | GET | Retrieves experiments related to a Statsig layer. |
| [Partially update a layer](actions/partially-update-a-layer-patch-console-v1-layers-id.md) | PUT | Updates a layer in Statsig. |
| [Update a layer](actions/update-a-layer-post-console-v1-layers-id.md) | PUT | Updates a layer in Statsig. |
| [Update Layer Overrides](actions/update-layer-overrides-post-console-v1-layers-id-overrides.md) | PUT | Updates layer overrides in Statsig. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Cancel archive a metric](actions/cancel-archive-a-metric-put-console-v1-metrics-id-cancel-archive.md) | DELETE | Cancels a metric archive in Statsig. |
| [Create Metric](actions/create-metric-post-console-v1-metrics.md) | POST | Creates a metric in Statsig. |
| [Create Metric Source](actions/create-metric-source-post-console-v1-metrics-metric-source.md) | POST | Creates a metric source in Statsig. |
| [Delete a metric](actions/delete-a-metric-delete-console-v1-metrics-id.md) | DELETE | Deletes a metric from Statsig. |
| [Delete Metric Source](actions/delete-metric-source-delete-console-v1-metrics-metric-source-name.md) | DELETE | Deletes a metric source from Statsig. |
| [Get SQL for a metric](actions/get-sql-for-a-metric-get-console-v1-metrics-id-sql.md) | GET | Retrieves SQL for a Statsig metric. |
| [Lineage: List experiments related to Metric](actions/lineage-list-experiments-related-to-metric-get-console-v1-metrics-id-experiments.md) | GET | Retrieves experiments related to a Statsig metric. |
| [List All Metric Values](actions/list-all-metric-values-get-console-v1-metrics-values.md) | GET | Retrieves all metric values from Statsig. |
| [List all Metrics](actions/list-all-metrics-get-console-v1-metrics-list.md) | GET | Retrieves all metrics from Statsig. |
| [List metric source](actions/list-metric-source-get-console-v1-metrics-metric-source-list.md) | GET | Retrieves metric sources from Statsig. |
| [Read Metric Definition by Name](actions/read-metric-definition-by-name-get-console-v1-metrics-name-type.md) | GET | Retrieves a metric definition by name from Statsig. |
| [Read Metric Definition](actions/read-metric-definition-get-console-v1-metrics-id.md) | GET | Retrieves a metric definition from Statsig. |
| [Read Metric Source](actions/read-metric-source-get-console-v1-metrics-metric-source-name.md) | GET | Retrieves a metric source from Statsig. |
| [Read Metric Source Metrics](actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics.md) | GET | Retrieves metric source metrics from Statsig. |
| [Read Single Metric Value](actions/read-single-metric-value-get-console-v1-metrics.md) | GET | Retrieves a single metric value from Statsig. |
| [Reload metric data](actions/reload-metric-data-post-console-v1-metrics-id-reload.md) | POST | Reloads metric data in Statsig. |
| [Schedule a metric archive](actions/schedule-a-metric-archive-put-console-v1-metrics-id-schedule-archive.md) | DELETE | Schedules a metric archive in Statsig. |
| [Unarchive a metric](actions/unarchive-a-metric-put-console-v1-metrics-id-unarchive.md) | PUT | Unarchives a metric in Statsig. |
| [Update a metric](actions/update-a-metric-post-console-v1-metrics-id.md) | PUT | Updates a metric in Statsig. |
| [Update Metric Source](actions/update-metric-source-post-console-v1-metrics-metric-source-name.md) | PUT | Updates a metric source in Statsig. |

### Param Store

| Action | Method | Description |
| --- | --- | --- |
| [Create Param Store](actions/create-param-store-post-console-v1-param-stores.md) | POST | Creates a param store in Statsig. |
| [Delete Param Store](actions/delete-param-store-delete-console-v1-param-stores-name.md) | DELETE | Deletes a param store from Statsig. |
| [Get Param Store](actions/get-param-store-get-console-v1-param-stores-name.md) | GET | Retrieves a param store from Statsig. |
| [List Param Stores](actions/list-param-stores-get-console-v1-param-stores.md) | GET | Retrieves param stores from Statsig. |
| [Update Param Store](actions/update-param-store-post-console-v1-param-stores-name.md) | PUT | Updates a param store in Statsig. |

### Privacy

| Action | Method | Description |
| --- | --- | --- |
| [Create User Data Deletion Request](actions/create-user-data-deletion-request-post-v1-delete-user-data.md) | POST | Creates a user data deletion request in Statsig. |
| [Get User Data Deletion Request Status](actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status.md) | GET | Retrieves a user data deletion request status from Statsig. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Info](actions/get-project-info-get-console-v1-project.md) | GET | Retrieves project info from Statsig. |

### Prompts

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt-post-console-v1-prompts.md) | POST | Creates a prompt in Statsig. |
| [Create Prompt Version](actions/create-prompt-version-post-console-v1-prompts-id-versions.md) | POST | Creates a prompt version in Statsig. |
| [Get Prompt](actions/get-prompt-get-console-v1-prompts-id.md) | GET | Retrieves a prompt from Statsig. |
| [List Prompts](actions/list-prompts-get-console-v1-prompts.md) | GET | Retrieves prompts from Statsig. |
| [Start Prompt Version Evaluation Job](actions/start-prompt-version-evaluation-job-post-console-v1-prompts-id-versions-versionid-start-ev.md) | PUT | Starts a prompt version evaluation job in Statsig. |
| [Update Prompt (partial)](actions/update-prompt-partial-patch-console-v1-prompts-id.md) | PUT | Updates a prompt in Statsig. |

### Release Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Abort Pipeline Trigger](actions/abort-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-abort.md) | PUT | Aborts a pipeline trigger in Statsig. |
| [Approve Pipeline Trigger Phase](actions/approve-pipeline-trigger-phase-put-console-v1-release-pipeline-triggers-id-approve.md) | PUT | Approves a pipeline trigger phase in Statsig. |
| [Create Pipeline](actions/create-pipeline-post-console-v1-release-pipelines.md) | POST | Creates a pipeline in Statsig. |
| [Delete Pipeline](actions/delete-pipeline-delete-console-v1-release-pipelines-id.md) | DELETE | Deletes a pipeline from Statsig. |
| [Fully Roll Out Pipeline Trigger](actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout.md) | PUT | Fully rolls out a pipeline trigger in Statsig. |
| [Get Pipeline](actions/get-pipeline-get-console-v1-release-pipelines-id.md) | GET | Retrieves a pipeline from Statsig. |
| [Get Pipeline Trigger](actions/get-pipeline-trigger-get-console-v1-release-pipeline-triggers-id.md) | GET | Retrieves a pipeline trigger from Statsig. |
| [List Pipeline Triggers](actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers.md) | GET | Retrieves pipeline triggers from Statsig. |
| [List Pipelines](actions/list-pipelines-get-console-v1-release-pipelines.md) | GET | Retrieves pipelines from Statsig. |
| [Pause Pipeline Trigger](actions/pause-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-pause.md) | PUT | Pauses a pipeline trigger in Statsig. |
| [Skip to Pipeline Trigger Phase](actions/skip-to-pipeline-trigger-phase-put-console-v1-release-pipeline-triggers-id-skip.md) | PUT | Skips to a pipeline trigger phase in Statsig. |
| [Unpause Pipeline Trigger](actions/unpause-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-unpause.md) | PUT | Unpauses a pipeline trigger in Statsig. |
| [Update Pipeline](actions/update-pipeline-post-console-v1-release-pipelines-id.md) | PUT | Updates a pipeline in Statsig. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Reports](actions/get-reports-get-console-v1-reports.md) | GET | Retrieves reports from Statsig. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role-post-console-v1-roles.md) | POST | Creates a role in Statsig. |
| [Delete Role](actions/delete-role-delete-console-v1-roles-id.md) | DELETE | Deletes a role from Statsig. |
| [Get Role](actions/get-role-get-console-v1-roles-id.md) | GET | Retrieves a role from Statsig. |
| [List Roles](actions/list-roles-get-console-v1-roles.md) | GET | Retrieves roles from Statsig. |
| [Update Role](actions/update-role-patch-console-v1-roles-id.md) | PUT | Updates a role in Statsig. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Add IDs to Segment](actions/add-ids-to-segment-patch-console-v1-segments-id-id-list.md) | POST | Adds IDs to a segment in Statsig. |
| [Add IDs to User Store ID List](actions/add-ids-to-user-store-id-list-patch-console-v1-segments-id-add-ids.md) | POST | Adds IDs to a user store ID list in Statsig. |
| [Archive Segment](actions/archive-segment-put-console-v1-segments-id-archive.md) | DELETE | Archives a segment in Statsig. |
| [Commit Segment Review](actions/commit-segment-review-put-console-v1-segments-id-reviews-reviewid-commit.md) | PUT | Commits a segment review in Statsig. |
| [Create Segment](actions/create-segment-post-console-v1-segments.md) | POST | Creates a segment in Statsig. |
| [Delete Segment](actions/delete-segment-delete-console-v1-segments-id.md) | DELETE | Deletes a segment from Statsig. |
| [Get ID List Metadata](actions/get-id-list-metadata-get-console-v1-segments-id-idlist-metadata.md) | GET | Retrieves an id list metadata from Statsig. |
| [Get IDs in a Segment](actions/get-ids-in-a-segment-get-console-v1-segments-id-id-list.md) | GET | Retrieves segment IDs from Statsig. |
| [Get Segment](actions/get-segment-get-console-v1-segments-id.md) | GET | Retrieves a segment from Statsig. |
| [List Segments](actions/list-segments-get-console-v1-segments.md) | GET | Retrieves segments from Statsig. |
| [Remove IDs from Segment](actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list.md) | DELETE | Removes IDs from a segment in Statsig. |
| [Remove IDs from User Store ID List](actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids.md) | DELETE | Removes IDs from a user store ID list in Statsig. |
| [Reset ID List Segment](actions/reset-id-list-segment-post-console-v1-segments-id-id-list-reset.md) | PUT | Resets an ID list segment in Statsig. |
| [Update Segment Rules](actions/update-segment-rules-post-console-v1-segments-id-conditional.md) | PUT | Updates segment rules in Statsig. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Settings](actions/get-project-settings-get-console-v1-settings-project.md) | GET | Retrieves project settings from Statsig. |
| [Get Reviews Settings](actions/get-reviews-settings-get-console-v1-settings-reviews.md) | GET | Retrieves reviews settings from Statsig. |
| [Get Roles Settings](actions/get-roles-settings-get-console-v1-settings-roles.md) | GET | Retrieves roles settings from Statsig. |
| [Get Teams Settings](actions/get-teams-settings-get-console-v1-settings-teams.md) | GET | Retrieves teams settings from Statsig. |
| [Update Project Settings](actions/update-project-settings-post-console-v1-settings-project.md) | PUT | Updates project settings in Statsig. |
| [Update Reviews Settings](actions/update-reviews-settings-post-console-v1-settings-reviews.md) | PUT | Updates review settings in Statsig. |
| [Update Roles Settings](actions/update-roles-settings-post-console-v1-settings-roles.md) | PUT | Updates role settings in Statsig. |
| [Update Teams Settings](actions/update-teams-settings-post-console-v1-settings-teams.md) | PUT | Updates team settings in Statsig. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag-post-console-v1-tags.md) | POST | Creates a tag in Statsig. |
| [Delete Tag](actions/delete-tag-delete-console-v1-tags-id.md) | DELETE | Deletes a tag from Statsig. |
| [List Tags](actions/list-tags-get-console-v1-tags.md) | GET | Retrieves tags from Statsig. |
| [Read Tag](actions/read-tag-get-console-v1-tags-id.md) | GET | Retrieves a tag from Statsig. |
| [Update Tag](actions/update-tag-patch-console-v1-tags-id.md) | PUT | Updates a tag in Statsig. |

### Target App

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Assign Target Apps](actions/bulk-assign-target-apps-patch-console-v1-target-app.md) | GET | Bulk assigns target apps in Statsig. |
| [Create Target App](actions/create-target-app-post-console-v1-target-app.md) | POST | Creates a target app in Statsig. |
| [Delete Target App](actions/delete-target-app-delete-console-v1-target-app-id.md) | DELETE | Deletes a target app from Statsig. |
| [List Target Apps](actions/list-target-apps-get-console-v1-target-app.md) | GET | Retrieves target apps from Statsig. |
| [Read Target App](actions/read-target-app-get-console-v1-target-app-id.md) | GET | Retrieves a target app from Statsig. |
| [Update Target App](actions/update-target-app-patch-console-v1-target-app-id.md) | PUT | Updates a target app in Statsig. |

### Unit Id Types

| Action | Method | Description |
| --- | --- | --- |
| [Create Unit ID Type](actions/create-unit-id-type-post-console-v1-unit-id-types.md) | POST | Creates a unit ID type in Statsig. |
| [Delete Unit ID Type](actions/delete-unit-id-type-delete-console-v1-unit-id-types-id.md) | DELETE | Deletes a unit ID type from Statsig. |
| [Get Unit ID Type](actions/get-unit-id-type-get-console-v1-unit-id-types-id.md) | GET | Retrieves a unit ID type from Statsig. |
| [List Unit ID Types](actions/list-unit-id-types-get-console-v1-unit-id-types.md) | GET | Retrieves unit id types from Statsig. |
| [Update Unit ID Type](actions/update-unit-id-type-patch-console-v1-unit-id-types-id.md) | PUT | Updates a unit ID type in Statsig. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Report in CSV format](actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report.md) | GET | Retrieves a report from Statsig in CSV format. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team-post-console-v1-users-teams.md) | POST | Creates a team in Statsig. |
| [Delete Team](actions/delete-team-delete-console-v1-users-teams-id.md) | DELETE | Deletes a team from Statsig. |
| [Get Team](actions/get-team-get-console-v1-users-teams-id.md) | GET | Retrieves a team from Statsig. |
| [Get user by email](actions/get-user-by-email-get-console-v1-users-email.md) | GET | Retrieves a user from Statsig by email. |
| [Get user by ID](actions/get-user-by-id-get-console-v1-users-id-id.md) | GET | Retrieves a user from Statsig by ID. |
| [Invite users](actions/invite-users-post-console-v1-users-invite.md) | POST | Invites users to Statsig. |
| [List Teams](actions/list-teams-get-console-v1-users-teams.md) | GET | Retrieves teams from Statsig. |
| [List Users](actions/list-users-get-console-v1-users.md) | GET | Retrieves users from Statsig. |
| [Update team](actions/update-team-patch-console-v1-users-teams-id.md) | PUT | Updates a team in Statsig. |
| [Update user](actions/update-user-post-console-v1-users-email.md) | PUT | Updates a user in Statsig. |

### Warehouse Connections

| Action | Method | Description |
| --- | --- | --- |
| [Update Warehouse Connection Parameters](actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections.md) | PUT | Updates warehouse connection parameters in Statsig. |

