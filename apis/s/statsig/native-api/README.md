# Statsig: Native API Reference

A consolidated summary of Statsig's API configuration and 279 documented operations, with links to official documentation.

- **Official docs:** https://docs.statsig.com/console-api/introduction
- **REST API base URL:** `https://statsigapi.net`
- **REST API base URL:** `https://api.statsig.com`
- **REST API base URL:** `https://events.statsigapi.net`

## Authentication

### Statsig Console API Key

Authenticate to the Statsig Console API with a Console API key sent in the STATSIG-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required · Statsig Console API key used as the STATSIG-API-KEY request header.
- **Server Secret Key:** `serverSecretKey` · required · Statsig Server Secret Key for HTTP API evaluation and event endpoints.
- **Client API Key:** `clientApiKey` · optional · Statsig Client SDK Key for client-safe HTTP API endpoints when applicable.

Send these headers with each API request:

```http
STATSIG-API-KEY: <apiKey>
statsig-api-key: <serverSecretKey>
```

[Official authentication documentation](https://docs.statsig.com/console-api/introduction)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `pagination.nextPage`. The current page number is read from `pagination.pageNumber`.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

- **REST API:** Send filters in the query string.

## Sorting

- **REST API:** Set the sort field with `sortBy` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (279 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Abandon Experiment](actions/abandon-experiment-put-console-v1-experiments-id-abandon.md) | `PUT /console/v1/experiments/{id}/abandon` | [docs](https://docs.statsig.com/api-reference/experiments/abandon-experiment) |
| [Abort Pipeline Trigger](actions/abort-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-abort.md) | `PUT /console/v1/release_pipeline_triggers/{id}/abort` | [docs](https://docs.statsig.com/api-reference/release-pipelines/abort-pipeline-trigger) |
| [Add Gate Overrides](actions/add-gate-overrides-patch-console-v1-gates-id-overrides.md) | `PATCH /console/v1/gates/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/gates/add-gate-overrides) |
| [Add Gate Rule](actions/add-gate-rule-post-console-v1-gates-id-rule.md) | `POST /console/v1/gates/{id}/rule` | [docs](https://docs.statsig.com/api-reference/gates/add-gate-rule) |
| [Add Holdout Overrides](actions/add-holdout-overrides-patch-console-v1-holdouts-id-overrides.md) | `PATCH /console/v1/holdouts/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/holdouts/add-holdout-overrides) |
| [Add IDs to Segment](actions/add-ids-to-segment-patch-console-v1-segments-id-id-list.md) | `PATCH /console/v1/segments/{id}/id_list` | [docs](https://docs.statsig.com/api-reference/segments/add-ids-to-segment) |
| [Add IDs to User Store ID List](actions/add-ids-to-user-store-id-list-patch-console-v1-segments-id-add-ids.md) | `PATCH /console/v1/segments/{id}/add_ids` | [docs](https://docs.statsig.com/api-reference/segments/add-ids-to-user-store-id-list) |
| [Add Layer Overrides](actions/add-layer-overrides-patch-console-v1-layers-id-overrides.md) | `PATCH /console/v1/layers/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/layers/add-layer-overrides) |
| [Add Widgets to Dashboard](actions/add-widgets-to-dashboard-post-console-v1-dashboards-id-widgets.md) | `POST /console/v1/dashboards/{id}/widgets` | [docs](https://docs.statsig.com/api-reference/dashboards/add-widgets-to-dashboard) |
| [Approve Pipeline Trigger Phase](actions/approve-pipeline-trigger-phase-put-console-v1-release-pipeline-triggers-id-approve.md) | `PUT /console/v1/release_pipeline_triggers/{id}/approve` | [docs](https://docs.statsig.com/api-reference/release-pipelines/approve-pipeline-trigger-phase) |
| [Archive Dynamic Config](actions/archive-dynamic-config-put-console-v1-dynamic-configs-id-archive.md) | `PUT /console/v1/dynamic_configs/{id}/archive` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/archive-dynamic-config) |
| [Archive Experiment](actions/archive-experiment-put-console-v1-experiments-id-archive.md) | `PUT /console/v1/experiments/{id}/archive` | [docs](https://docs.statsig.com/api-reference/experiments/archive-experiment) |
| [Archive Gate](actions/archive-gate-put-console-v1-gates-id-archive.md) | `PUT /console/v1/gates/{id}/archive` | [docs](https://docs.statsig.com/api-reference/gates/archive-gate) |
| [Archive Segment](actions/archive-segment-put-console-v1-segments-id-archive.md) | `PUT /console/v1/segments/{id}/archive` | [docs](https://docs.statsig.com/api-reference/segments/archive-segment) |
| [Backfill Ingestion](actions/backfill-ingestion-post-console-v1-ingestion-backfill.md) | `POST /console/v1/ingestion/backfill` | [docs](https://docs.statsig.com/api-reference/ingestions/backfill-ingestion) |
| [Bulk Assign Target Apps](actions/bulk-assign-target-apps-patch-console-v1-target-app.md) | `PATCH /console/v1/target_app` | [docs](https://docs.statsig.com/api-reference/target-app/bulk-assign-target-apps) |
| [Cancel archive a metric](actions/cancel-archive-a-metric-put-console-v1-metrics-id-cancel-archive.md) | `PUT /console/v1/metrics/{id}/cancel_archive` | [docs](https://docs.statsig.com/api-reference/metrics/cancel-archive-a-metric) |
| [Cancel Pulse Load (Warehouse Native)](actions/cancel-pulse-load-warehouse-native-post-console-v1-experiments-id-pulse-load-history-dagid.md) | `POST /console/v1/experiments/{id}/pulse_load_history/{dagID}/cancel` | [docs](https://docs.statsig.com/api-reference/experiments/cancel-pulse-load-warehouse-native) |
| [Change Validation](actions/change-validation-post-console-v1-change-validation.md) | `POST /console/v1/change_validation` | [docs](https://docs.statsig.com/api-reference/change-validation/change-validation) |
| [Check Feature Gates](actions/check-feature-gates-post-v1-check-gate.md) | `POST /v1/check_gate` | [docs](https://docs.statsig.com/api-reference/feature-gates/check-feature-gates) |
| [Commit Dynamic Config Review](actions/commit-dynamic-config-review-put-console-v1-dynamic-configs-id-reviews-reviewid-commit.md) | `PUT /console/v1/dynamic_configs/{id}/reviews/{reviewID}/commit` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/commit-dynamic-config-review) |
| [Commit Experiment Review](actions/commit-experiment-review-put-console-v1-experiments-id-reviews-reviewid-commit.md) | `PUT /console/v1/experiments/{id}/reviews/{reviewID}/commit` | [docs](https://docs.statsig.com/api-reference/experiments/commit-experiment-review) |
| [Commit Gate Review](actions/commit-gate-review-put-console-v1-gates-id-reviews-reviewid-commit.md) | `PUT /console/v1/gates/{id}/reviews/{reviewID}/commit` | [docs](https://docs.statsig.com/api-reference/gates/commit-gate-review) |
| [Commit Segment Review](actions/commit-segment-review-put-console-v1-segments-id-reviews-reviewid-commit.md) | `PUT /console/v1/segments/{id}/reviews/{reviewID}/commit` | [docs](https://docs.statsig.com/api-reference/segments/commit-segment-review) |
| [Conclude Experiment & Defer Decision](actions/conclude-experiment-defer-decision-put-console-v1-experiments-id-defer-decision.md) | `PUT /console/v1/experiments/{id}/defer_decision` | [docs](https://docs.statsig.com/api-reference/experiments/conclude-experiment-defer-decision) |
| [Create a Layer](actions/create-a-layer-post-console-v1-layers.md) | `POST /console/v1/layers` | [docs](https://docs.statsig.com/api-reference/layers/create-a-layer) |
| [Create Assignment Source](actions/create-assignment-source-post-console-v1-experiments-assignment-sources.md) | `POST /console/v1/experiments/assignment_sources` | [docs](https://docs.statsig.com/api-reference/experiments/create-assignment-source) |
| [Create Autotune](actions/create-autotune-post-console-v1-autotunes.md) | `POST /console/v1/autotunes` | [docs](https://docs.statsig.com/api-reference/autotunes/create-autotune) |
| [Create Dashboard](actions/create-dashboard-post-console-v1-dashboards.md) | `POST /console/v1/dashboards` | [docs](https://docs.statsig.com/api-reference/dashboards/create-dashboard) |
| [Create Dynamic Config](actions/create-dynamic-config-post-console-v1-dynamic-configs.md) | `POST /console/v1/dynamic_configs` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/create-dynamic-config) |
| [Create Entity Property Source](actions/create-entity-property-source-post-console-v1-experiments-entity-properties.md) | `POST /console/v1/experiments/entity_properties` | [docs](https://docs.statsig.com/api-reference/experiments/create-entity-property-source) |
| [Create Experiment](actions/create-experiment-post-console-v1-experiments.md) | `POST /console/v1/experiments` | [docs](https://docs.statsig.com/api-reference/experiments/create-experiment) |
| [Create Gate](actions/create-gate-post-console-v1-gates.md) | `POST /console/v1/gates` | [docs](https://docs.statsig.com/api-reference/gates/create-gate) |
| [Create holdout](actions/create-holdout-post-console-v1-holdouts.md) | `POST /console/v1/holdouts` | [docs](https://docs.statsig.com/api-reference/holdouts/create-holdout) |
| [Create Ingestion Databricks](actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks.md) | `POST /console/v1/ingestion/connection/databricks` | [docs](https://docs.statsig.com/api-reference/ingestions/create-ingestion-databricks) |
| [Create Ingestion Source](actions/create-ingestion-source-post-console-v1-ingestion.md) | `POST /console/v1/ingestion` | [docs](https://docs.statsig.com/api-reference/ingestions/create-ingestion-source) |
| [Create Key](actions/create-key-post-console-v1-keys.md) | `POST /console/v1/keys` | [docs](https://docs.statsig.com/api-reference/keys/create-key) |
| [Create Metric](actions/create-metric-post-console-v1-metrics.md) | `POST /console/v1/metrics` | [docs](https://docs.statsig.com/api-reference/metrics/create-metric) |
| [Create Metric Source](actions/create-metric-source-post-console-v1-metrics-metric-source.md) | `POST /console/v1/metrics/metric_source` | [docs](https://docs.statsig.com/api-reference/metrics/create-metric-source) |
| [Create Param Store](actions/create-param-store-post-console-v1-param-stores.md) | `POST /console/v1/param_stores` | [docs](https://docs.statsig.com/api-reference/param-store/create-param-store) |
| [Create Pipeline](actions/create-pipeline-post-console-v1-release-pipelines.md) | `POST /console/v1/release_pipelines` | [docs](https://docs.statsig.com/api-reference/release-pipelines/create-pipeline) |
| [Create Prompt](actions/create-prompt-post-console-v1-prompts.md) | `POST /console/v1/prompts` | [docs](https://docs.statsig.com/api-reference/prompts/create-prompt) |
| [Create Prompt Version](actions/create-prompt-version-post-console-v1-prompts-id-versions.md) | `POST /console/v1/prompts/{id}/versions` | [docs](https://docs.statsig.com/api-reference/prompts/create-prompt-version) |
| [Create Qualifying Event](actions/create-qualifying-event-post-console-v1-experiments-qualifying-events.md) | `POST /console/v1/experiments/qualifying_events` | [docs](https://docs.statsig.com/api-reference/experiments-warehouse-native/create-qualifying-event) |
| [Create Role](actions/create-role-post-console-v1-roles.md) | `POST /console/v1/roles` | [docs](https://docs.statsig.com/api-reference/roles/create-role) |
| [Create Segment](actions/create-segment-post-console-v1-segments.md) | `POST /console/v1/segments` | [docs](https://docs.statsig.com/api-reference/segments/create-segment) |
| [Create Tag](actions/create-tag-post-console-v1-tags.md) | `POST /console/v1/tags` | [docs](https://docs.statsig.com/api-reference/tags/create-tag) |
| [Create Target App](actions/create-target-app-post-console-v1-target-app.md) | `POST /console/v1/target_app` | [docs](https://docs.statsig.com/api-reference/target-app/create-target-app) |
| [Create Team](actions/create-team-post-console-v1-users-teams.md) | `POST /console/v1/users/teams` | [docs](https://docs.statsig.com/api-reference/users/create-team) |
| [Create Unit ID Type](actions/create-unit-id-type-post-console-v1-unit-id-types.md) | `POST /console/v1/unit_id_types` | [docs](https://docs.statsig.com/api-reference/unit-id-types/create-unit-id-type) |
| [Create User Data Deletion Request](actions/create-user-data-deletion-request-post-v1-delete-user-data.md) | `POST /v1/delete_user_data` | [docs](https://docs.statsig.com/compliance/user_data_deletion_requests/) |
| [Deactivate Key](actions/deactivate-key-patch-console-v1-keys-id-deactivate.md) | `PATCH /console/v1/keys/{id}/deactivate` | [docs](https://docs.statsig.com/api-reference/keys/deactivate-key) |
| [Delete a layer](actions/delete-a-layer-delete-console-v1-layers-id.md) | `DELETE /console/v1/layers/{id}` | [docs](https://docs.statsig.com/api-reference/layers/delete-a-layer) |
| [Delete a metric](actions/delete-a-metric-delete-console-v1-metrics-id.md) | `DELETE /console/v1/metrics/{id}` | [docs](https://docs.statsig.com/api-reference/metrics/delete-a-metric) |
| [Delete Assignment Source](actions/delete-assignment-source-delete-console-v1-experiments-assignment-source-name.md) | `DELETE /console/v1/experiments/assignment_source/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/delete-assignment-source) |
| [Delete Autotune](actions/delete-autotune-delete-console-v1-autotunes-id.md) | `DELETE /console/v1/autotunes/{id}` | [docs](https://docs.statsig.com/api-reference/autotunes/delete-autotune) |
| [Delete Dynamic Config](actions/delete-dynamic-config-delete-console-v1-dynamic-configs-id.md) | `DELETE /console/v1/dynamic_configs/{id}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/delete-dynamic-config) |
| [Delete Dynamic Config Rule](actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid.md) | `DELETE /console/v1/dynamic_configs/{id}/rule/{ruleId}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/delete-dynamic-config-rule) |
| [Delete Entity Property Source](actions/delete-entity-property-source-delete-console-v1-experiments-entity-property-name.md) | `DELETE /console/v1/experiments/entity_property/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/delete-entity-property-source) |
| [Delete Experiment Overrides](actions/delete-experiment-overrides-delete-console-v1-experiments-id-overrides.md) | `DELETE /console/v1/experiments/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/experiments/delete-experiment-overrides) |
| [Delete Gate Overrides](actions/delete-gate-overrides-delete-console-v1-gates-id-overrides.md) | `DELETE /console/v1/gates/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/gates/delete-gate-overrides) |
| [Delete Gate Rule](actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid.md) | `DELETE /console/v1/gates/{id}/rules/{ruleID}` | [docs](https://docs.statsig.com/api-reference/gates/delete-gate-rule) |
| [Delete Gates](actions/delete-gates-delete-console-v1-gates-id.md) | `DELETE /console/v1/gates/{id}` | [docs](https://docs.statsig.com/api-reference/gates/delete-gates) |
| [Delete holdout by id](actions/delete-holdout-by-id-delete-console-v1-holdouts-id.md) | `DELETE /console/v1/holdouts/{id}` | [docs](https://docs.statsig.com/api-reference/holdouts/delete-holdout-by-id) |
| [Delete Ingestion Source](actions/delete-ingestion-source-delete-console-v1-ingestion.md) | `DELETE /console/v1/ingestion` | [docs](https://docs.statsig.com/api-reference/ingestions/delete-ingestion-source) |
| [Delete Key](actions/delete-key-delete-console-v1-keys-id.md) | `DELETE /console/v1/keys/{id}` | [docs](https://docs.statsig.com/api-reference/keys/delete-key) |
| [Delete Layer Overrides](actions/delete-layer-overrides-delete-console-v1-layers-id-overrides.md) | `DELETE /console/v1/layers/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/layers/delete-layer-overrides) |
| [Delete Metric Source](actions/delete-metric-source-delete-console-v1-metrics-metric-source-name.md) | `DELETE /console/v1/metrics/metric_source/{name}` | [docs](https://docs.statsig.com/api-reference/metrics/delete-metric-source) |
| [Delete Param Store](actions/delete-param-store-delete-console-v1-param-stores-name.md) | `DELETE /console/v1/param_stores/{name}` | [docs](https://docs.statsig.com/api-reference/param-store/delete-param-store) |
| [Delete Pipeline](actions/delete-pipeline-delete-console-v1-release-pipelines-id.md) | `DELETE /console/v1/release_pipelines/{id}` | [docs](https://docs.statsig.com/api-reference/release-pipelines/delete-pipeline) |
| [Delete Qualifying Event](actions/delete-qualifying-event-delete-console-v1-experiments-qualifying-events-name.md) | `DELETE /console/v1/experiments/qualifying_events/{name}` | [docs](https://docs.statsig.com/api-reference/experiments-warehouse-native/delete-qualifying-event) |
| [Delete Role](actions/delete-role-delete-console-v1-roles-id.md) | `DELETE /console/v1/roles/{id}` | [docs](https://docs.statsig.com/api-reference/roles/delete-role) |
| [Delete Segment](actions/delete-segment-delete-console-v1-segments-id.md) | `DELETE /console/v1/segments/{id}` | [docs](https://docs.statsig.com/api-reference/segments/delete-segment) |
| [Delete Tag](actions/delete-tag-delete-console-v1-tags-id.md) | `DELETE /console/v1/tags/{id}` | [docs](https://docs.statsig.com/api-reference/tags/delete-tag) |
| [Delete Target App](actions/delete-target-app-delete-console-v1-target-app-id.md) | `DELETE /console/v1/target_app/{id}` | [docs](https://docs.statsig.com/api-reference/target-app/delete-target-app) |
| [Delete Team](actions/delete-team-delete-console-v1-users-teams-id.md) | `DELETE /console/v1/users/teams/{id}` | [docs](https://docs.statsig.com/api-reference/users/delete-team) |
| [Delete Unit ID Type](actions/delete-unit-id-type-delete-console-v1-unit-id-types-id.md) | `DELETE /console/v1/unit_id_types/{id}` | [docs](https://docs.statsig.com/api-reference/unit-id-types/delete-unit-id-type) |
| [Deleted Experiment](actions/deleted-experiment-delete-console-v1-experiments-id.md) | `DELETE /console/v1/experiments/{id}` | [docs](https://docs.statsig.com/api-reference/experiments/deleted-experiment) |
| [Disable Dynamic Config](actions/disable-dynamic-config-put-console-v1-dynamic-configs-id-disable.md) | `PUT /console/v1/dynamic_configs/{id}/disable` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/disable-dynamic-config) |
| [Disable Experiment Groups](actions/disable-experiment-groups-post-console-v1-experiments-id-disable-groups.md) | `POST /console/v1/experiments/{id}/disable_groups` | [docs](https://docs.statsig.com/api-reference/experiments/disable-experiment-groups) |
| [Disable Gate](actions/disable-gate-put-console-v1-gates-id-disable.md) | `PUT /console/v1/gates/{id}/disable` | [docs](https://docs.statsig.com/api-reference/gates/disable-gate) |
| [Enable Dynamic Config](actions/enable-dynamic-config-put-console-v1-dynamic-configs-id-enable.md) | `PUT /console/v1/dynamic_configs/{id}/enable` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/enable-dynamic-config) |
| [Enable Experiment Groups](actions/enable-experiment-groups-post-console-v1-experiments-id-enable-groups.md) | `POST /console/v1/experiments/{id}/enable_groups` | [docs](https://docs.statsig.com/api-reference/experiments/enable-experiment-groups) |
| [Enable Gate](actions/enable-gate-put-console-v1-gates-id-enable.md) | `PUT /console/v1/gates/{id}/enable` | [docs](https://docs.statsig.com/api-reference/gates/enable-gate) |
| [Finish Experiment Early](actions/finish-experiment-early-put-console-v1-autotunes-id-make-decision.md) | `PUT /console/v1/autotunes/{id}/make_decision` | [docs](https://docs.statsig.com/api-reference/autotunes/finish-experiment-early) |
| [Finish Experiment Early](actions/finish-experiment-early-put-console-v1-experiments-id-make-decision.md) | `PUT /console/v1/experiments/{id}/make_decision` | [docs](https://docs.statsig.com/api-reference/experiments/finish-experiment-early) |
| [Fully Roll Out Pipeline Trigger](actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout.md) | `PUT /console/v1/release_pipeline_triggers/{id}/rollout` | [docs](https://docs.statsig.com/api-reference/release-pipelines/fully-roll-out-pipeline-trigger) |
| [Fully Update Autotune](actions/fully-update-autotune-post-console-v1-autotunes-id.md) | `POST /console/v1/autotunes/{id}` | [docs](https://docs.statsig.com/api-reference/autotunes/fully-update-autotune) |
| [Fully Update Dynamic Config](actions/fully-update-dynamic-config-post-console-v1-dynamic-configs-id.md) | `POST /console/v1/dynamic_configs/{id}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/fully-update-dynamic-config) |
| [Fully Update Experiment](actions/fully-update-experiment-post-console-v1-experiments-id.md) | `POST /console/v1/experiments/{id}` | [docs](https://docs.statsig.com/api-reference/experiments/fully-update-experiment) |
| [Fully Update Gates](actions/fully-update-gates-post-console-v1-gates-id.md) | `POST /console/v1/gates/{id}` | [docs](https://docs.statsig.com/api-reference/gates/fully-update-gates) |
| [Get Company Info](actions/get-company-info-get-console-v1-company.md) | `GET /console/v1/company` | [docs](https://docs.statsig.com/api-reference/company/get-company-info) |
| [Get Dynamic Config](actions/get-dynamic-config-get-console-v1-dynamic-configs-id.md) | `GET /console/v1/dynamic_configs/{id}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/get-dynamic-config) |
| [Get Dynamic Config or Experiment](actions/get-dynamic-config-or-experiment-post-v1-get-config.md) | `POST /v1/get_config` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/get-dynamic-config-or-experiment) |
| [Get Dynamic Config Rules](actions/get-dynamic-config-rules-get-console-v1-dynamic-configs-id-rules.md) | `GET /console/v1/dynamic_configs/{id}/rules` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/get-dynamic-config-rules) |
| [Get Entity Property Source](actions/get-entity-property-source-get-console-v1-experiments-entity-property-name.md) | `GET /console/v1/experiments/entity_property/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/get-entity-property-source) |
| [Get Environments](actions/get-environments-get-console-v1-environments.md) | `GET /console/v1/environments` | [docs](https://docs.statsig.com/api-reference/environments/get-environments) |
| [Get Experiment Context](actions/get-experiment-context-get-console-v1-experiments-id-context.md) | `GET /console/v1/experiments/{id}/context` | [docs](https://docs.statsig.com/api-reference/experiments/get-experiment-context) |
| [Get Experiment](actions/get-experiment-get-console-v1-experiments-id.md) | `GET /console/v1/experiments/{id}` | [docs](https://docs.statsig.com/api-reference/experiments/get-experiment) |
| [Get Experiment Guardrail Alert Statuses](actions/get-experiment-guardrail-alert-statuses-get-console-v1-experiments-id-alerts.md) | `GET /console/v1/experiments/{id}/alerts` | [docs](https://docs.statsig.com/api-reference/experiments/get-experiment-guardrail-alert-statuses) |
| [Get Experiment Overrides](actions/get-experiment-overrides-get-console-v1-experiments-id-overrides.md) | `GET /console/v1/experiments/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/experiments/get-experiment-overrides) |
| [Get Gate Override](actions/get-gate-override-get-console-v1-gates-id-overrides.md) | `GET /console/v1/gates/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/gates/get-gate-override) |
| [Get holdout by id](actions/get-holdout-by-id-get-console-v1-holdouts-id.md) | `GET /console/v1/holdouts/{id}` | [docs](https://docs.statsig.com/api-reference/holdouts/get-holdout-by-id) |
| [Get ID List Metadata](actions/get-id-list-metadata-get-console-v1-segments-id-idlist-metadata.md) | `GET /console/v1/segments/{id}/idlist_metadata` | [docs](https://docs.statsig.com/api-reference/segments/get-id-list-metadata) |
| [Get IDs in a Segment](actions/get-ids-in-a-segment-get-console-v1-segments-id-id-list.md) | `GET /console/v1/segments/{id}/id_list` | [docs](https://docs.statsig.com/api-reference/segments/get-ids-in-a-segment) |
| [Get Ingestion Event Count](actions/get-ingestion-event-count-get-console-v1-ingestion-events-count.md) | `GET /console/v1/ingestion/events/count` | [docs](https://docs.statsig.com/api-reference/ingestions/get-ingestion-event-count) |
| [Get Ingestion Event Delta Ledger](actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta.md) | `GET /console/v1/ingestion/events/delta` | [docs](https://docs.statsig.com/api-reference/ingestions/get-ingestion-event-delta-ledger) |
| [Get Layer Overrides](actions/get-layer-overrides-get-console-v1-layers-id-overrides.md) | `GET /console/v1/layers/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/layers/get-layer-overrides) |
| [Get Layer Parameters](actions/get-layer-parameters-post-v1-get-layer.md) | `POST /v1/get_layer` | [docs](https://docs.statsig.com/api-reference/layers/get-layer-parameters) |
| [Get Layers](actions/get-layers-get-console-v1-layers.md) | `GET /console/v1/layers` | [docs](https://docs.statsig.com/api-reference/layers/get-layers) |
| [Get metrics using event name](actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics.md) | `GET /console/v1/events/{eventName}/metrics` | [docs](https://docs.statsig.com/api-reference/events/get-metrics-using-event-name) |
| [Get one layer](actions/get-one-layer-get-console-v1-layers-id.md) | `GET /console/v1/layers/{id}` | [docs](https://docs.statsig.com/api-reference/layers/get-one-layer) |
| [Get Param Store](actions/get-param-store-get-console-v1-param-stores-name.md) | `GET /console/v1/param_stores/{name}` | [docs](https://docs.statsig.com/api-reference/param-store/get-param-store) |
| [Get Pipeline](actions/get-pipeline-get-console-v1-release-pipelines-id.md) | `GET /console/v1/release_pipelines/{id}` | [docs](https://docs.statsig.com/api-reference/release-pipelines/get-pipeline) |
| [Get Pipeline Trigger](actions/get-pipeline-trigger-get-console-v1-release-pipeline-triggers-id.md) | `GET /console/v1/release_pipeline_triggers/{id}` | [docs](https://docs.statsig.com/api-reference/release-pipelines/get-pipeline-trigger) |
| [Get Project Info](actions/get-project-info-get-console-v1-project.md) | `GET /console/v1/project` | [docs](https://docs.statsig.com/api-reference/project/get-project-info) |
| [Get Project Settings](actions/get-project-settings-get-console-v1-settings-project.md) | `GET /console/v1/settings/project` | [docs](https://docs.statsig.com/api-reference/settings/get-project-settings) |
| [Get Prompt](actions/get-prompt-get-console-v1-prompts-id.md) | `GET /console/v1/prompts/{id}` | [docs](https://docs.statsig.com/api-reference/prompts/get-prompt) |
| [Get Pulse Load History Details (Warehouse Native)](actions/get-pulse-load-history-details-warehouse-native-get-console-v1-experiments-id-pulse-load-h.md) | `GET /console/v1/experiments/{id}/pulse_load_history/{dagID}` | [docs](https://docs.statsig.com/api-reference/experiments/get-pulse-load-history-details-warehouse-native) |
| [Get Ranked List for Contextual Bandit](actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list.md) | `POST /v1/get_ranked_list` | [docs](https://docs.statsig.com/api-reference/autotune/get-ranked-list-for-contextual-bandit) |
| [Get Report in CSV format](actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report.md) | `GET /console/v1/project/usage_billing/report` | [docs](https://docs.statsig.com/api-reference/usage/get-report-in-csv-format) |
| [Get Reports](actions/get-reports-get-console-v1-reports.md) | `GET /console/v1/reports` | [docs](https://docs.statsig.com/api-reference/reports/get-reports) |
| [Get Reviews Settings](actions/get-reviews-settings-get-console-v1-settings-reviews.md) | `GET /console/v1/settings/reviews` | [docs](https://docs.statsig.com/api-reference/settings/get-reviews-settings) |
| [Get Role](actions/get-role-get-console-v1-roles-id.md) | `GET /console/v1/roles/{id}` | [docs](https://docs.statsig.com/api-reference/roles/get-role) |
| [Get Roles Settings](actions/get-roles-settings-get-console-v1-settings-roles.md) | `GET /console/v1/settings/roles` | [docs](https://docs.statsig.com/api-reference/settings/get-roles-settings) |
| [Get Segment](actions/get-segment-get-console-v1-segments-id.md) | `GET /console/v1/segments/{id}` | [docs](https://docs.statsig.com/api-reference/segments/get-segment) |
| [Get Specific Dynamic Config Rule](actions/get-specific-dynamic-config-rule-get-console-v1-dynamic-configs-id-rule-ruleid.md) | `GET /console/v1/dynamic_configs/{id}/rule/{ruleId}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/get-specific-dynamic-config-rule) |
| [Get specific events](actions/get-specific-events-get-console-v1-events-eventname.md) | `GET /console/v1/events/{eventName}` | [docs](https://docs.statsig.com/api-reference/events/get-specific-events) |
| [Get SQL for a metric](actions/get-sql-for-a-metric-get-console-v1-metrics-id-sql.md) | `GET /console/v1/metrics/{id}/sql` | [docs](https://docs.statsig.com/api-reference/metrics/get-sql-for-a-metric) |
| [Get Team](actions/get-team-get-console-v1-users-teams-id.md) | `GET /console/v1/users/teams/{id}` | [docs](https://docs.statsig.com/api-reference/users/get-team) |
| [Get Teams Settings](actions/get-teams-settings-get-console-v1-settings-teams.md) | `GET /console/v1/settings/teams` | [docs](https://docs.statsig.com/api-reference/settings/get-teams-settings) |
| [Get Unit ID Type](actions/get-unit-id-type-get-console-v1-unit-id-types-id.md) | `GET /console/v1/unit_id_types/{id}` | [docs](https://docs.statsig.com/api-reference/unit-id-types/get-unit-id-type) |
| [Get user by email](actions/get-user-by-email-get-console-v1-users-email.md) | `GET /console/v1/users/{email}` | [docs](https://docs.statsig.com/api-reference/users/get-user-by-email) |
| [Get user by ID](actions/get-user-by-id-get-console-v1-users-id-id.md) | `GET /console/v1/users/id/{id}` | [docs](https://docs.statsig.com/api-reference/users/get-user-by-id) |
| [Get User Data Deletion Request Status](actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status.md) | `POST /v1/get_delete_user_data_request_status` | [docs](https://docs.statsig.com/compliance/user_data_deletion_requests/) |
| [Invite users](actions/invite-users-post-console-v1-users-invite.md) | `POST /console/v1/users/invite` | [docs](https://docs.statsig.com/api-reference/users/invite-users) |
| [Launch Gate](actions/launch-gate-put-console-v1-gates-id-launch.md) | `PUT /console/v1/gates/{id}/launch` | [docs](https://docs.statsig.com/api-reference/gates/launch-gate) |
| [Lineage: List Experiment related to Layer](actions/lineage-list-experiment-related-to-layer-get-console-v1-layers-id-experiments.md) | `GET /console/v1/layers/{id}/experiments` | [docs](https://docs.statsig.com/api-reference/layers/lineage-list-experiment-related-to-layer) |
| [Lineage: List experiments related to Metric](actions/lineage-list-experiments-related-to-metric-get-console-v1-metrics-id-experiments.md) | `GET /console/v1/metrics/{id}/experiments` | [docs](https://docs.statsig.com/api-reference/metrics/lineage-list-experiments-related-to-metric) |
| [List All Metric Values](actions/list-all-metric-values-get-console-v1-metrics-values.md) | `GET /console/v1/metrics/values` | [docs](https://docs.statsig.com/api-reference/metrics/list-all-metric-values) |
| [List all Metrics](actions/list-all-metrics-get-console-v1-metrics-list.md) | `GET /console/v1/metrics/list` | [docs](https://docs.statsig.com/api-reference/metrics/list-all-metrics) |
| [List Assignment Sources](actions/list-assignment-sources-get-console-v1-experiments-assignment-sources.md) | `GET /console/v1/experiments/assignment_sources` | [docs](https://docs.statsig.com/api-reference/experiments/list-assignment-sources) |
| [List Audit Logs](actions/list-audit-logs-get-console-v1-audit-logs.md) | `GET /console/v1/audit_logs` | [docs](https://docs.statsig.com/api-reference/audit-logs/list-audit-logs) |
| [List Autotune](actions/list-autotune-get-console-v1-autotunes.md) | `GET /console/v1/autotunes` | [docs](https://docs.statsig.com/api-reference/autotunes/list-autotune) |
| [List Dashboards](actions/list-dashboards-get-console-v1-dashboards.md) | `GET /console/v1/dashboards` | [docs](https://docs.statsig.com/api-reference/dashboards/list-dashboards) |
| [List Dynamic Config References](actions/list-dynamic-config-references-get-console-v1-gates-id-dynamic-config-references.md) | `GET /console/v1/gates/{id}/dynamic_config_references` | [docs](https://docs.statsig.com/api-reference/gates/list-dynamic-config-references) |
| [List Dynamic Config Versions](actions/list-dynamic-config-versions-get-console-v1-dynamic-configs-id-versions.md) | `GET /console/v1/dynamic_configs/{id}/versions` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/list-dynamic-config-versions) |
| [List Dynamic Configs](actions/list-dynamic-configs-get-console-v1-dynamic-configs.md) | `GET /console/v1/dynamic_configs` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/list-dynamic-configs) |
| [List Entity Property Sources](actions/list-entity-property-sources-get-console-v1-experiments-entity-properties.md) | `GET /console/v1/experiments/entity_properties` | [docs](https://docs.statsig.com/api-reference/experiments/list-entity-property-sources) |
| [List Events](actions/list-events-get-console-v1-events.md) | `GET /console/v1/events` | [docs](https://docs.statsig.com/api-reference/events/list-events) |
| [List Experiment References](actions/list-experiment-references-get-console-v1-gates-id-experiment-references.md) | `GET /console/v1/gates/{id}/experiment_references` | [docs](https://docs.statsig.com/api-reference/gates/list-experiment-references) |
| [List Experiment Versions](actions/list-experiment-versions-get-console-v1-experiments-id-versions.md) | `GET /console/v1/experiments/{id}/versions` | [docs](https://docs.statsig.com/api-reference/experiments/list-experiment-versions) |
| [List Experiments](actions/list-experiments-get-console-v1-experiments.md) | `GET /console/v1/experiments` | [docs](https://docs.statsig.com/api-reference/experiments/list-experiments) |
| [List Gate References](actions/list-gate-references-get-console-v1-gates-id-gate-references.md) | `GET /console/v1/gates/{id}/gate_references` | [docs](https://docs.statsig.com/api-reference/gates/list-gate-references) |
| [List Gate Versions](actions/list-gate-versions-get-console-v1-gates-id-versions.md) | `GET /console/v1/gates/{id}/versions` | [docs](https://docs.statsig.com/api-reference/gates/list-gate-versions) |
| [List Gates](actions/list-gates-get-console-v1-gates.md) | `GET /console/v1/gates` | [docs](https://docs.statsig.com/api-reference/gates/list-gates) |
| [List Holdouts](actions/list-holdouts-get-console-v1-holdouts.md) | `GET /console/v1/holdouts` | [docs](https://docs.statsig.com/api-reference/holdouts/list-holdouts) |
| [List Ingestion Runs](actions/list-ingestion-runs-get-console-v1-ingestion-runs.md) | `GET /console/v1/ingestion/runs` | [docs](https://docs.statsig.com/api-reference/ingestions/list-ingestion-runs) |
| [List Ingestions Status](actions/list-ingestions-status-get-console-v1-ingestion-status.md) | `GET /console/v1/ingestion/status` | [docs](https://docs.statsig.com/api-reference/ingestions/list-ingestions-status) |
| [List Keys](actions/list-keys-get-console-v1-keys.md) | `GET /console/v1/keys` | [docs](https://docs.statsig.com/api-reference/keys/list-keys) |
| [List metric source](actions/list-metric-source-get-console-v1-metrics-metric-source-list.md) | `GET /console/v1/metrics/metric_source/list` | [docs](https://docs.statsig.com/api-reference/metrics/list-metric-source) |
| [List Param Stores](actions/list-param-stores-get-console-v1-param-stores.md) | `GET /console/v1/param_stores` | [docs](https://docs.statsig.com/api-reference/param-store/list-param-stores) |
| [List Pipeline Triggers](actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers.md) | `GET /console/v1/release_pipeline_triggers` | [docs](https://docs.statsig.com/api-reference/release-pipelines/list-pipeline-triggers) |
| [List Pipelines](actions/list-pipelines-get-console-v1-release-pipelines.md) | `GET /console/v1/release_pipelines` | [docs](https://docs.statsig.com/api-reference/release-pipelines/list-pipelines) |
| [List Prompts](actions/list-prompts-get-console-v1-prompts.md) | `GET /console/v1/prompts` | [docs](https://docs.statsig.com/api-reference/prompts/list-prompts) |
| [List qualifying event](actions/list-qualifying-event-get-console-v1-experiments-qualifying-events.md) | `GET /console/v1/experiments/qualifying_events` | [docs](https://docs.statsig.com/api-reference/experiments-warehouse-native/list-qualifying-event) |
| [List Roles](actions/list-roles-get-console-v1-roles.md) | `GET /console/v1/roles` | [docs](https://docs.statsig.com/api-reference/roles/list-roles) |
| [List Segments](actions/list-segments-get-console-v1-segments.md) | `GET /console/v1/segments` | [docs](https://docs.statsig.com/api-reference/segments/list-segments) |
| [List Tags](actions/list-tags-get-console-v1-tags.md) | `GET /console/v1/tags` | [docs](https://docs.statsig.com/api-reference/tags/list-tags) |
| [List Target Apps](actions/list-target-apps-get-console-v1-target-app.md) | `GET /console/v1/target_app` | [docs](https://docs.statsig.com/api-reference/target-app/list-target-apps) |
| [List Teams](actions/list-teams-get-console-v1-users-teams.md) | `GET /console/v1/users/teams` | [docs](https://docs.statsig.com/api-reference/users/list-teams) |
| [List Topline Alert Events](actions/list-topline-alert-events-get-console-v1-alerts-id-events.md) | `GET /console/v1/alerts/{id}/events` | [docs](https://docs.statsig.com/api-reference/alerts/list-topline-alert-events) |
| [List Topline Alerts](actions/list-topline-alerts-get-console-v1-alerts.md) | `GET /console/v1/alerts` | [docs](https://docs.statsig.com/api-reference/alerts/list-topline-alerts) |
| [List Unit ID Types](actions/list-unit-id-types-get-console-v1-unit-id-types.md) | `GET /console/v1/unit_id_types` | [docs](https://docs.statsig.com/api-reference/unit-id-types/list-unit-id-types) |
| [List Users](actions/list-users-get-console-v1-users.md) | `GET /console/v1/users` | [docs](https://docs.statsig.com/api-reference/users/list-users) |
| [Load Pulse Gate](actions/load-pulse-gate-post-console-v1-gates-id-load-pulse.md) | `POST /console/v1/gates/{id}/load_pulse` | [docs](https://docs.statsig.com/api-reference/gates/load-pulse-gate) |
| [Load Pulse (Warehouse Native)](actions/load-pulse-warehouse-native-post-console-v1-experiments-id-load-pulse.md) | `POST /console/v1/experiments/{id}/load_pulse` | [docs](https://docs.statsig.com/api-reference/experiments/load-pulse-warehouse-native) |
| [Log Custom Events](actions/log-custom-events-post-v1-log-event.md) | `POST /v1/log_event` | [docs](https://docs.statsig.com/api-reference/events/log-custom-events) |
| [Log Custom Exposure Events](actions/log-custom-exposure-events-post-v1-log-custom-exposure.md) | `POST /v1/log_custom_exposure` | [docs](https://docs.statsig.com/api-reference/events/log-custom-exposure-events) |
| [Partially update a layer](actions/partially-update-a-layer-patch-console-v1-layers-id.md) | `PATCH /console/v1/layers/{id}` | [docs](https://docs.statsig.com/api-reference/layers/partially-update-a-layer) |
| [Partially Update Autotune](actions/partially-update-autotune-patch-console-v1-autotunes-id.md) | `PATCH /console/v1/autotunes/{id}` | [docs](https://docs.statsig.com/api-reference/autotunes/partially-update-autotune) |
| [Partially Update Dynamic Config](actions/partially-update-dynamic-config-patch-console-v1-dynamic-configs-id.md) | `PATCH /console/v1/dynamic_configs/{id}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/partially-update-dynamic-config) |
| [Partially Update Experiment Overrides](actions/partially-update-experiment-overrides-patch-console-v1-experiments-id-overrides.md) | `PATCH /console/v1/experiments/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/experiments/partially-update-experiment-overrides) |
| [Partially Update Experiment](actions/partially-update-experiment-patch-console-v1-experiments-id.md) | `PATCH /console/v1/experiments/{id}` | [docs](https://docs.statsig.com/api-reference/experiments/partially-update-experiment) |
| [Partially Update Gates](actions/partially-update-gates-patch-console-v1-gates-id.md) | `PATCH /console/v1/gates/{id}` | [docs](https://docs.statsig.com/api-reference/gates/partially-update-gates) |
| [Partially update holdout by id](actions/partially-update-holdout-by-id-patch-console-v1-holdouts-id.md) | `PATCH /console/v1/holdouts/{id}` | [docs](https://docs.statsig.com/api-reference/holdouts/partially-update-holdout-by-id) |
| [Patch Assignment Source](actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name.md) | `PATCH /console/v1/experiments/assignment_source/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/patch-assignment-source) |
| [Patch Entity Property Source](actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name.md) | `PATCH /console/v1/experiments/entity_property/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/patch-entity-property-source) |
| [Pause Pipeline Trigger](actions/pause-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-pause.md) | `PUT /console/v1/release_pipeline_triggers/{id}/pause` | [docs](https://docs.statsig.com/api-reference/release-pipelines/pause-pipeline-trigger) |
| [Post Assignment Source](actions/post-assignment-source-post-console-v1-experiments-assignment-source-name.md) | `POST /console/v1/experiments/assignment_source/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/post-assignment-source) |
| [Post Entity Property Source](actions/post-entity-property-source-post-console-v1-experiments-entity-property-name.md) | `POST /console/v1/experiments/entity_property/{name}` | [docs](https://docs.statsig.com/api-reference/experiments/post-entity-property-source) |
| [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-experiments-id-pulse-load-history.md) | `GET /console/v1/experiments/{id}/pulse_load_history` | [docs](https://docs.statsig.com/api-reference/experiments/pulse-load-history-warehouse-native) |
| [Pulse Load History (Warehouse Native)](actions/pulse-load-history-warehouse-native-get-console-v1-gates-id-rules-ruleid-pulse-load-histor.md) | `GET /console/v1/gates/{id}/rules/{ruleID}/pulse_load_history` | [docs](https://docs.statsig.com/api-reference/gates/pulse-load-history-warehouse-native) |
| [Read Autotune](actions/read-autotune-get-console-v1-autotunes-id.md) | `GET /console/v1/autotunes/{id}` | [docs](https://docs.statsig.com/api-reference/autotunes/read-autotune) |
| [Read Dashboard](actions/read-dashboard-get-console-v1-dashboards-id.md) | `GET /console/v1/dashboards/{id}` | [docs](https://docs.statsig.com/api-reference/dashboards/read-dashboard) |
| [Read Dashboard Widget Results](actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results.md) | `GET /console/v1/dashboards/{id}/widgets/{widgetId}/results` | [docs](https://docs.statsig.com/api-reference/dashboards/read-dashboard-widget-results) |
| [Read Exposure Event Count](actions/read-exposure-event-count-get-console-v1-exposure-count.md) | `GET /console/v1/exposure_count` | [docs](https://docs.statsig.com/api-reference/configs/read-exposure-event-count) |
| [Read Gate Checks](actions/read-gate-checks-get-console-v1-gates-id-checks.md) | `GET /console/v1/gates/{id}/checks` | [docs](https://docs.statsig.com/api-reference/gates/read-gate-checks) |
| [Read Gate](actions/read-gate-get-console-v1-gates-id.md) | `GET /console/v1/gates/{id}` | [docs](https://docs.statsig.com/api-reference/gates/read-gate) |
| [Read Gate Rules](actions/read-gate-rules-get-console-v1-gates-id-rules.md) | `GET /console/v1/gates/{id}/rules` | [docs](https://docs.statsig.com/api-reference/gates/read-gate-rules) |
| [Read Holdout Overrides](actions/read-holdout-overrides-get-console-v1-holdouts-id-overrides.md) | `GET /console/v1/holdouts/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/holdouts/read-holdout-overrides) |
| [Read Ingestion](actions/read-ingestion-get-console-v1-ingestion.md) | `GET /console/v1/ingestion` | [docs](https://docs.statsig.com/api-reference/ingestions/read-ingestion) |
| [Read Ingestion Run](actions/read-ingestion-run-get-console-v1-ingestion-runs-id.md) | `GET /console/v1/ingestion/runs/{id}` | [docs](https://docs.statsig.com/api-reference/ingestions/read-ingestion-run) |
| [Read Ingestion Schedule](actions/read-ingestion-schedule-get-console-v1-ingestion-schedule.md) | `GET /console/v1/ingestion/schedule` | [docs](https://docs.statsig.com/api-reference/ingestions/read-ingestion-schedule) |
| [Read Key](actions/read-key-get-console-v1-keys-id.md) | `GET /console/v1/keys/{id}` | [docs](https://docs.statsig.com/api-reference/keys/read-key) |
| [Read Metric Definition by Name](actions/read-metric-definition-by-name-get-console-v1-metrics-name-type.md) | `GET /console/v1/metrics/{name}/{type}` | [docs](https://docs.statsig.com/api-reference/metrics/read-metric-definition-by-name) |
| [Read Metric Definition](actions/read-metric-definition-get-console-v1-metrics-id.md) | `GET /console/v1/metrics/{id}` | [docs](https://docs.statsig.com/api-reference/metrics/read-metric-definition) |
| [Read Metric Source](actions/read-metric-source-get-console-v1-metrics-metric-source-name.md) | `GET /console/v1/metrics/metric_source/{name}` | [docs](https://docs.statsig.com/api-reference/metrics/read-metric-source) |
| [Read Metric Source Metrics](actions/read-metric-source-metrics-get-console-v1-metrics-metric-source-name-metrics.md) | `GET /console/v1/metrics/metric_source/{name}/metrics` | [docs](https://docs.statsig.com/api-reference/metrics/read-metric-source-metrics) |
| [Read Qualifying Event](actions/read-qualifying-event-get-console-v1-experiments-qualifying-events-name.md) | `GET /console/v1/experiments/qualifying_events/{name}` | [docs](https://docs.statsig.com/api-reference/experiments-warehouse-native/read-qualifying-event) |
| [Read Single Metric Value](actions/read-single-metric-value-get-console-v1-metrics.md) | `GET /console/v1/metrics` | [docs](https://docs.statsig.com/api-reference/metrics/read-single-metric-value) |
| [Read Tag](actions/read-tag-get-console-v1-tags-id.md) | `GET /console/v1/tags/{id}` | [docs](https://docs.statsig.com/api-reference/tags/read-tag) |
| [Read Target App](actions/read-target-app-get-console-v1-target-app-id.md) | `GET /console/v1/target_app/{id}` | [docs](https://docs.statsig.com/api-reference/target-app/read-target-app) |
| [Read Topline Alert Event](actions/read-topline-alert-event-get-console-v1-alerts-id-events-eventid.md) | `GET /console/v1/alerts/{id}/events/{eventId}` | [docs](https://docs.statsig.com/api-reference/alerts/read-topline-alert-event) |
| [Read Topline Alert](actions/read-topline-alert-get-console-v1-alerts-id.md) | `GET /console/v1/alerts/{id}` | [docs](https://docs.statsig.com/api-reference/alerts/read-topline-alert) |
| [Reload metric data](actions/reload-metric-data-post-console-v1-metrics-id-reload.md) | `POST /console/v1/metrics/{id}/reload` | [docs](https://docs.statsig.com/api-reference/metrics/reload-metric-data) |
| [Remove Holdout Overrides](actions/remove-holdout-overrides-delete-console-v1-holdouts-id-overrides.md) | `DELETE /console/v1/holdouts/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/holdouts/remove-holdout-overrides) |
| [Remove IDs from Segment](actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list.md) | `DELETE /console/v1/segments/{id}/id_list` | [docs](https://docs.statsig.com/api-reference/segments/remove-ids-from-segment) |
| [Remove IDs from User Store ID List](actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids.md) | `PATCH /console/v1/segments/{id}/remove_ids` | [docs](https://docs.statsig.com/api-reference/segments/remove-ids-from-user-store-id-list) |
| [Replace Widgets on Dashboard](actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets.md) | `PUT /console/v1/dashboards/{id}/widgets` | [docs](https://docs.statsig.com/api-reference/dashboards/replace-widgets-on-dashboard) |
| [Reset Experiment](actions/reset-experiment-put-console-v1-autotunes-id-reset.md) | `PUT /console/v1/autotunes/{id}/reset` | [docs](https://docs.statsig.com/api-reference/autotunes/reset-experiment) |
| [Reset Experiment](actions/reset-experiment-put-console-v1-experiments-id-reset.md) | `PUT /console/v1/experiments/{id}/reset` | [docs](https://docs.statsig.com/api-reference/experiments/reset-experiment) |
| [Reset ID List Segment](actions/reset-id-list-segment-post-console-v1-segments-id-id-list-reset.md) | `POST /console/v1/segments/{id}/id_list/reset` | [docs](https://docs.statsig.com/api-reference/segments/reset-id-list-segment) |
| [Resolve Metric Rollout Alert](actions/resolve-metric-rollout-alert-post-console-v1-experiments-id-alerts-metricid-resolve.md) | `POST /console/v1/experiments/{id}/alerts/{metricId}/resolve` | [docs](https://docs.statsig.com/api-reference/experiments/resolve-metric-rollout-alert) |
| [Resolve Metric Rollout Alert](actions/resolve-metric-rollout-alert-post-console-v1-gates-id-alerts-metricid-resolve.md) | `POST /console/v1/gates/{id}/alerts/{metricId}/resolve` | [docs](https://docs.statsig.com/api-reference/gates/resolve-metric-rollout-alert) |
| [Restart As New Experiment](actions/restart-as-new-experiment-post-console-v1-experiments-id-restart-as-new.md) | `POST /console/v1/experiments/{id}/restart_as_new` | [docs](https://docs.statsig.com/api-reference/experiments/restart-as-new-experiment) |
| [Retrieve cumulative exposures](actions/retrieve-cumulative-exposures-get-console-v1-experiments-id-cumulative-exposures.md) | `GET /console/v1/experiments/{id}/cumulative_exposures` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-cumulative-exposures) |
| [Retrieve Experiment Checks Diagnostics](actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks.md) | `GET /console/v1/experiments/{id}/diagnostics_checks` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-experiment-checks-diagnostics) |
| [Retrieve Experiment Summary Charts (Beta)](actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts.md) | `GET /console/v1/experiments/{id}/summary_charts` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-experiment-summary-charts-beta) |
| [Retrieve Exposures By Dimension](actions/retrieve-exposures-by-dimension-get-console-v1-experiments-id-dimensional-exposures.md) | `GET /console/v1/experiments/{id}/dimensional_exposures` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-exposures-by-dimension) |
| [Retrieve Pulse Metric Result](actions/retrieve-pulse-metric-result-get-console-v1-experiments-id-pulse-metric-result.md) | `GET /console/v1/experiments/{id}/pulse_metric_result` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-pulse-metric-result) |
| [Retrieve Pulse Results (Beta)](actions/retrieve-pulse-results-beta-get-console-v1-experiments-id-pulse-results.md) | `GET /console/v1/experiments/{id}/pulse_results` | [docs](https://docs.statsig.com/api-reference/experiments/retrieve-pulse-results-beta) |
| [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results.md) | `GET /console/v1/gates/{id}/rules/{ruleID}/pulse_results` | [docs](https://docs.statsig.com/api-reference/gates/retrieve-pulse-results) |
| [Retrieve Pulse Results](actions/retrieve-pulse-results-get-console-v1-holdouts-id-pulse-results.md) | `GET /console/v1/holdouts/{id}/pulse_results` | [docs](https://docs.statsig.com/api-reference/holdouts/retrieve-pulse-results) |
| [Rotate Key](actions/rotate-key-patch-console-v1-keys-id-rotate.md) | `PATCH /console/v1/keys/{id}/rotate` | [docs](https://docs.statsig.com/api-reference/keys/rotate-key) |
| [Schedule a metric archive](actions/schedule-a-metric-archive-put-console-v1-metrics-id-schedule-archive.md) | `PUT /console/v1/metrics/{id}/schedule_archive` | [docs](https://docs.statsig.com/api-reference/metrics/schedule-a-metric-archive) |
| [Schedule Experiment Start](actions/schedule-experiment-start-post-console-v1-experiments-id-schedule-start.md) | `POST /console/v1/experiments/{id}/schedule_start` | [docs](https://docs.statsig.com/api-reference/experiments/schedule-experiment-start) |
| [Skip to Pipeline Trigger Phase](actions/skip-to-pipeline-trigger-phase-put-console-v1-release-pipeline-triggers-id-skip.md) | `PUT /console/v1/release_pipeline_triggers/{id}/skip` | [docs](https://docs.statsig.com/api-reference/release-pipelines/skip-to-pipeline-trigger-phase) |
| [Start Autotune Experiment](actions/start-autotune-experiment-put-console-v1-autotunes-id-start.md) | `PUT /console/v1/autotunes/{id}/start` | [docs](https://docs.statsig.com/api-reference/autotunes/start-autotune-experiment) |
| [Start Experiment Code Cleanup](actions/start-experiment-code-cleanup-post-console-v1-experiments-id-code-cleanup.md) | `POST /console/v1/experiments/{id}/code_cleanup` | [docs](https://docs.statsig.com/api-reference/experiments/start-experiment-code-cleanup) |
| [Start Experiment](actions/start-experiment-put-console-v1-experiments-id-start.md) | `PUT /console/v1/experiments/{id}/start` | [docs](https://docs.statsig.com/api-reference/experiments/start-experiment) |
| [Start Gate Code Cleanup](actions/start-gate-code-cleanup-post-console-v1-gates-id-code-cleanup.md) | `POST /console/v1/gates/{id}/code_cleanup` | [docs](https://docs.statsig.com/api-reference/gates/start-gate-code-cleanup) |
| [Start Prompt Version Evaluation Job](actions/start-prompt-version-evaluation-job-post-console-v1-prompts-id-versions-versionid-start-ev.md) | `POST /console/v1/prompts/{id}/versions/{versionId}/start_evals` | [docs](https://docs.statsig.com/api-reference/prompts/start-prompt-version-evaluation-job) |
| [Unarchive a metric](actions/unarchive-a-metric-put-console-v1-metrics-id-unarchive.md) | `PUT /console/v1/metrics/{id}/unarchive` | [docs](https://docs.statsig.com/api-reference/metrics/unarchive-a-metric) |
| [Unarchive Dynamic Config](actions/unarchive-dynamic-config-put-console-v1-dynamic-configs-id-unarchive.md) | `PUT /console/v1/dynamic_configs/{id}/unarchive` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/unarchive-dynamic-config) |
| [Unarchive Experiment](actions/unarchive-experiment-put-console-v1-experiments-id-unarchive.md) | `PUT /console/v1/experiments/{id}/unarchive` | [docs](https://docs.statsig.com/api-reference/experiments/unarchive-experiment) |
| [Unarchive Gate](actions/unarchive-gate-put-console-v1-gates-id-unarchive.md) | `PUT /console/v1/gates/{id}/unarchive` | [docs](https://docs.statsig.com/api-reference/gates/unarchive-gate) |
| [Unpause Pipeline Trigger](actions/unpause-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-unpause.md) | `PUT /console/v1/release_pipeline_triggers/{id}/unpause` | [docs](https://docs.statsig.com/api-reference/release-pipelines/unpause-pipeline-trigger) |
| [Update a layer](actions/update-a-layer-post-console-v1-layers-id.md) | `POST /console/v1/layers/{id}` | [docs](https://docs.statsig.com/api-reference/layers/update-a-layer) |
| [Update a metric](actions/update-a-metric-post-console-v1-metrics-id.md) | `POST /console/v1/metrics/{id}` | [docs](https://docs.statsig.com/api-reference/metrics/update-a-metric) |
| [Update change validation message](actions/update-change-validation-message-patch-console-v1-change-validation-message.md) | `PATCH /console/v1/change_validation/message` | [docs](https://docs.statsig.com/api-reference/change-validation/update-change-validation-message) |
| [Update Dynamic Config Rule By Id](actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid.md) | `PATCH /console/v1/dynamic_configs/{id}/rule/{ruleId}` | [docs](https://docs.statsig.com/api-reference/dynamic-configs/update-dynamic-config-rule-by-id) |
| [Update Environments](actions/update-environments-post-console-v1-environments.md) | `POST /console/v1/environments` | [docs](https://docs.statsig.com/api-reference/environments/update-environments) |
| [Update Experiment Overrides](actions/update-experiment-overrides-post-console-v1-experiments-id-overrides.md) | `POST /console/v1/experiments/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/experiments/update-experiment-overrides) |
| [Update Gate Overrides](actions/update-gate-overrides-post-console-v1-gates-id-overrides.md) | `POST /console/v1/gates/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/gates/update-gate-overrides) |
| [Update Gate Rules](actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid.md) | `PATCH /console/v1/gates/{id}/rules/{ruleID}` | [docs](https://docs.statsig.com/api-reference/gates/update-gate-rules) |
| [Update holdout by id](actions/update-holdout-by-id-post-console-v1-holdouts-id.md) | `POST /console/v1/holdouts/{id}` | [docs](https://docs.statsig.com/api-reference/holdouts/update-holdout-by-id) |
| [Update Holdout Overrides](actions/update-holdout-overrides-post-console-v1-holdouts-id-overrides.md) | `POST /console/v1/holdouts/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/holdouts/update-holdout-overrides) |
| [Update Ingestion Schedule](actions/update-ingestion-schedule-post-console-v1-ingestion-schedule.md) | `POST /console/v1/ingestion/schedule` | [docs](https://docs.statsig.com/api-reference/ingestions/update-ingestion-schedule) |
| [Update Ingestion Source](actions/update-ingestion-source-patch-console-v1-ingestion.md) | `PATCH /console/v1/ingestion` | [docs](https://docs.statsig.com/api-reference/ingestions/update-ingestion-source) |
| [Update Key](actions/update-key-patch-console-v1-keys-id.md) | `PATCH /console/v1/keys/{id}` | [docs](https://docs.statsig.com/api-reference/keys/update-key) |
| [Update Layer Overrides](actions/update-layer-overrides-post-console-v1-layers-id-overrides.md) | `POST /console/v1/layers/{id}/overrides` | [docs](https://docs.statsig.com/api-reference/layers/update-layer-overrides) |
| [Update Metric Source](actions/update-metric-source-post-console-v1-metrics-metric-source-name.md) | `POST /console/v1/metrics/metric_source/{name}` | [docs](https://docs.statsig.com/api-reference/metrics/update-metric-source) |
| [Update Param Store](actions/update-param-store-post-console-v1-param-stores-name.md) | `POST /console/v1/param_stores/{name}` | [docs](https://docs.statsig.com/api-reference/param-store/update-param-store) |
| [Update Pipeline](actions/update-pipeline-post-console-v1-release-pipelines-id.md) | `POST /console/v1/release_pipelines/{id}` | [docs](https://docs.statsig.com/api-reference/release-pipelines/update-pipeline) |
| [Update Project Settings](actions/update-project-settings-post-console-v1-settings-project.md) | `POST /console/v1/settings/project` | [docs](https://docs.statsig.com/api-reference/settings/update-project-settings) |
| [Update Prompt (partial)](actions/update-prompt-partial-patch-console-v1-prompts-id.md) | `PATCH /console/v1/prompts/{id}` | [docs](https://docs.statsig.com/api-reference/prompts/update-prompt-partial) |
| [Update Qualifying Event](actions/update-qualifying-event-post-console-v1-experiments-qualifying-events-name.md) | `POST /console/v1/experiments/qualifying_events/{name}` | [docs](https://docs.statsig.com/api-reference/experiments-warehouse-native/update-qualifying-event) |
| [Update Reviews Settings](actions/update-reviews-settings-post-console-v1-settings-reviews.md) | `POST /console/v1/settings/reviews` | [docs](https://docs.statsig.com/api-reference/settings/update-reviews-settings) |
| [Update Role](actions/update-role-patch-console-v1-roles-id.md) | `PATCH /console/v1/roles/{id}` | [docs](https://docs.statsig.com/api-reference/roles/update-role) |
| [Update Roles Settings](actions/update-roles-settings-post-console-v1-settings-roles.md) | `POST /console/v1/settings/roles` | [docs](https://docs.statsig.com/api-reference/settings/update-roles-settings) |
| [Update Segment Rules](actions/update-segment-rules-post-console-v1-segments-id-conditional.md) | `POST /console/v1/segments/{id}/conditional` | [docs](https://docs.statsig.com/api-reference/segments/update-segment-rules) |
| [Update Tag](actions/update-tag-patch-console-v1-tags-id.md) | `PATCH /console/v1/tags/{id}` | [docs](https://docs.statsig.com/api-reference/tags/update-tag) |
| [Update Target App](actions/update-target-app-patch-console-v1-target-app-id.md) | `PATCH /console/v1/target_app/{id}` | [docs](https://docs.statsig.com/api-reference/target-app/update-target-app) |
| [Update team](actions/update-team-patch-console-v1-users-teams-id.md) | `PATCH /console/v1/users/teams/{id}` | [docs](https://docs.statsig.com/api-reference/users/update-team) |
| [Update Teams Settings](actions/update-teams-settings-post-console-v1-settings-teams.md) | `POST /console/v1/settings/teams` | [docs](https://docs.statsig.com/api-reference/settings/update-teams-settings) |
| [Update Unit ID Type](actions/update-unit-id-type-patch-console-v1-unit-id-types-id.md) | `PATCH /console/v1/unit_id_types/{id}` | [docs](https://docs.statsig.com/api-reference/unit-id-types/update-unit-id-type) |
| [Update user](actions/update-user-post-console-v1-users-email.md) | `POST /console/v1/users/{email}` | [docs](https://docs.statsig.com/api-reference/users/update-user) |
| [Update Warehouse Connection Parameters](actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections.md) | `PATCH /console/v1/wh_connections` | [docs](https://docs.statsig.com/api-reference/warehouse-connections/update-warehouse-connection-parameters) |
