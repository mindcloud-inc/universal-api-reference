# Statsig Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Statsig expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ids-in-a-segment-get-console-v1-segments-id-id-list?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Statsig actions that support pagination

- [Get IDs in a Segment](actions/get-ids-in-a-segment-get-console-v1-segments-id-id-list.md)
- [Get Layers](actions/get-layers-get-console-v1-layers.md)
- [Get metrics using event name](actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics.md)
- [Get specific events](actions/get-specific-events-get-console-v1-events-eventname.md)
- [Lineage: List Experiment related to Layer](actions/lineage-list-experiment-related-to-layer-get-console-v1-layers-id-experiments.md)
- [Lineage: List experiments related to Metric](actions/lineage-list-experiments-related-to-metric-get-console-v1-metrics-id-experiments.md)
- [List All Metric Values](actions/list-all-metric-values-get-console-v1-metrics-values.md)
- [List all Metrics](actions/list-all-metrics-get-console-v1-metrics-list.md)
- [List Assignment Sources](actions/list-assignment-sources-get-console-v1-experiments-assignment-sources.md)
- [List Audit Logs](actions/list-audit-logs-get-console-v1-audit-logs.md)
- [List Autotune](actions/list-autotune-get-console-v1-autotunes.md)
- [List Dashboards](actions/list-dashboards-get-console-v1-dashboards.md)
- [List Dynamic Config References](actions/list-dynamic-config-references-get-console-v1-gates-id-dynamic-config-references.md)
- [List Dynamic Config Versions](actions/list-dynamic-config-versions-get-console-v1-dynamic-configs-id-versions.md)
- [List Dynamic Configs](actions/list-dynamic-configs-get-console-v1-dynamic-configs.md)
- [List Entity Property Sources](actions/list-entity-property-sources-get-console-v1-experiments-entity-properties.md)
- [List Events](actions/list-events-get-console-v1-events.md)
- [List Experiment References](actions/list-experiment-references-get-console-v1-gates-id-experiment-references.md)
- [List Experiment Versions](actions/list-experiment-versions-get-console-v1-experiments-id-versions.md)
- [List Experiments](actions/list-experiments-get-console-v1-experiments.md)
- [List Gate References](actions/list-gate-references-get-console-v1-gates-id-gate-references.md)
- [List Gate Versions](actions/list-gate-versions-get-console-v1-gates-id-versions.md)
- [List Gates](actions/list-gates-get-console-v1-gates.md)
- [List Holdouts](actions/list-holdouts-get-console-v1-holdouts.md)
- [List Keys](actions/list-keys-get-console-v1-keys.md)
- [List metric source](actions/list-metric-source-get-console-v1-metrics-metric-source-list.md)
- [List Param Stores](actions/list-param-stores-get-console-v1-param-stores.md)
- [List Pipeline Triggers](actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers.md)
- [List Pipelines](actions/list-pipelines-get-console-v1-release-pipelines.md)
- [List Prompts](actions/list-prompts-get-console-v1-prompts.md)
- [List qualifying event](actions/list-qualifying-event-get-console-v1-experiments-qualifying-events.md)
- [List Roles](actions/list-roles-get-console-v1-roles.md)
- [List Segments](actions/list-segments-get-console-v1-segments.md)
- [List Tags](actions/list-tags-get-console-v1-tags.md)
- [List Target Apps](actions/list-target-apps-get-console-v1-target-app.md)
- [List Teams](actions/list-teams-get-console-v1-users-teams.md)
- [List Topline Alert Events](actions/list-topline-alert-events-get-console-v1-alerts-id-events.md)
- [List Topline Alerts](actions/list-topline-alerts-get-console-v1-alerts.md)
- [List Unit ID Types](actions/list-unit-id-types-get-console-v1-unit-id-types.md)
- [List Users](actions/list-users-get-console-v1-users.md)
- [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-experiments-id-pulse-load-history.md)
- [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-gates-id-rules-ruleid-pulse-load-histor.md)
- [Read Metric Source Metrics](actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics.md)
