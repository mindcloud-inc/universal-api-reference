# GrowthBook: Native API Reference

A consolidated summary of GrowthBook's API configuration and 179 documented operations, with links to official documentation.

- **Official docs:** https://docs.growthbook.io/api
- **OpenAPI specification:** https://api.growthbook.io/api/v1/openapi.yaml
- **API base URL:** `https://api.growthbook.io/api/v1`

## Authentication

### API Key

Use a GrowthBook secret key. MindCloud will send it as Authorization: Bearer <apiKey>, which matches GrowthBook's bearer auth contract.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.growthbook.io/api#authentication)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (179 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a target rule to a ramp schedule](actions/add-target-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/add-target` | [docs](https://docs.growthbook.io/api) |
| [Add members to team](actions/add-team-members.md) | `POST /teams/:id/members` | [docs](https://docs.growthbook.io/api) |
| [Approve the current pending-approval step](actions/approve-step-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/approve-step` | [docs](https://docs.growthbook.io/api) |
| [Bulk create or update experiment templates](actions/bulk-import-experiment-templates.md) | `POST /experiment-templates/bulk-import` | [docs](https://docs.growthbook.io/api) |
| [Complete a ramp schedule immediately](actions/complete-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/complete` | [docs](https://docs.growthbook.io/api) |
| [Create a single customField](actions/create-custom-field.md) | `POST /custom-fields` | [docs](https://docs.growthbook.io/api) |
| [Create a single dashboard](actions/create-dashboard.md) | `POST /dashboards` | [docs](https://docs.growthbook.io/api) |
| [Create a single experimentTemplate](actions/create-experiment-template.md) | `POST /experiment-templates` | [docs](https://docs.growthbook.io/api) |
| [Create a single metricGroup](actions/create-metric-group.md) | `POST /metric-groups` | [docs](https://docs.growthbook.io/api) |
| [Create a single rampSchedule](actions/create-ramp-schedule.md) | `POST /ramp-schedules` | [docs](https://docs.growthbook.io/api) |
| [Create a single rampScheduleTemplate](actions/create-ramp-schedule-template.md) | `POST /ramp-schedule-templates` | [docs](https://docs.growthbook.io/api) |
| [Create a single team](actions/create-team.md) | `POST /teams` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single archetype](actions/delete-archetype.md) | `DELETE /archetypes/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single attribute](actions/delete-attribute.md) | `DELETE /attributes/:property` | [docs](https://docs.growthbook.io/api) |
| [Delete a single customField](actions/delete-custom-field.md) | `DELETE /custom-fields/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single dashboard](actions/delete-dashboard.md) | `DELETE /dashboards/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single dimension](actions/delete-dimension.md) | `DELETE /dimensions/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single environment](actions/delete-environment.md) | `DELETE /environments/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single experimentTemplate](actions/delete-experiment-template.md) | `DELETE /experiment-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single fact metric](actions/delete-fact-metric.md) | `DELETE /fact-metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single fact table](actions/delete-fact-table.md) | `DELETE /fact-tables/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single fact table filter](actions/delete-fact-table-filter.md) | `DELETE /fact-tables/:factTableId/filters/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single feature](actions/delete-feature.md) | `DELETE /features/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a rule from a draft revision](actions/delete-feature-revision-rule.md) | `DELETE /features/:id/revisions/:version/rules/:ruleId` | [docs](https://docs.growthbook.io/api) |
| [Remove ramp schedule from a rule](actions/delete-feature-revision-rule-ramp-schedule.md) | `DELETE /features/:id/revisions/:version/rules/:ruleId/ramp-schedule` | [docs](https://docs.growthbook.io/api) |
| [Removes a single user from an organization](actions/delete-member.md) | `DELETE /members/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a metric](actions/delete-metric.md) | `DELETE /metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single metricGroup](actions/delete-metric-group.md) | `DELETE /metric-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single rampSchedule](actions/delete-ramp-schedule.md) | `DELETE /ramp-schedules/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single rampScheduleTemplate](actions/delete-ramp-schedule-template.md) | `DELETE /ramp-schedule-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single saved group](actions/delete-saved-group.md) | `DELETE /saved-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single SDK connection](actions/delete-sdk-connection.md) | `DELETE /sdk-connections/:id` | [docs](https://docs.growthbook.io/api) |
| [Deletes a single segment](actions/delete-segment.md) | `DELETE /segments/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a single team](actions/delete-team.md) | `DELETE /teams/:id` | [docs](https://docs.growthbook.io/api) |
| [Delete a variation screenshot](actions/delete-variation-screenshot.md) | `DELETE /experiments/:id/variation/:variationId/screenshot` | [docs](https://docs.growthbook.io/api) |
| [Remove a target rule from a ramp schedule](actions/eject-target-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/eject-target` | [docs](https://docs.growthbook.io/api) |
| [Get a single archetype](actions/get-archetype.md) | `GET /archetypes/:id` | [docs](https://docs.growthbook.io/api) |
| [Get list of code references for a single feature id](actions/get-code-refs.md) | `GET /code-refs/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single customField](actions/get-custom-field.md) | `GET /custom-fields/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single dashboard](actions/get-dashboard.md) | `GET /dashboards/:id` | [docs](https://docs.growthbook.io/api) |
| [Get all dashboards for an experiment](actions/get-dashboards-for-experiment.md) | `GET /dashboards/by-experiment/:experimentId` | [docs](https://docs.growthbook.io/api) |
| [Get a single data source](actions/get-data-source.md) | `GET /data-sources/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single dimension](actions/get-dimension.md) | `GET /dimensions/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single experiment](actions/get-experiment.md) | `GET /experiments/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a list of experiments with names and ids](actions/get-experiment-names.md) | `GET /experiment-names` | [docs](https://docs.growthbook.io/api) |
| [Get results for an experiment](actions/get-experiment-results.md) | `GET /experiments/:id/results` | [docs](https://docs.growthbook.io/api) |
| [Get an experiment snapshot status](actions/get-experiment-snapshot.md) | `GET /snapshots/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single experimentTemplate](actions/get-experiment-template.md) | `GET /experiment-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single fact metric](actions/get-fact-metric.md) | `GET /fact-metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single fact table](actions/get-fact-table.md) | `GET /fact-tables/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single fact filter](actions/get-fact-table-filter.md) | `GET /fact-tables/:factTableId/filters/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single feature](actions/get-feature.md) | `GET /features/:id` | [docs](https://docs.growthbook.io/api) |
| [Get list of feature keys](actions/get-feature-keys.md) | `GET /feature-keys` | [docs](https://docs.growthbook.io/api) |
| [Get a single feature revision](actions/get-feature-revision.md) | `GET /features/:id/revisions/:version` | [docs](https://docs.growthbook.io/api) |
| [Get the most recent active draft revision](actions/get-feature-revision-latest.md) | `GET /features/:id/revisions/latest` | [docs](https://docs.growthbook.io/api) |
| [Get merge status for a draft revision](actions/get-feature-revision-merge-status.md) | `GET /features/:id/revisions/:version/merge-status` | [docs](https://docs.growthbook.io/api) |
| [List revisions for a feature](actions/get-feature-revisions.md) | `GET /features/:id/revisions` | [docs](https://docs.growthbook.io/api) |
| [Get stale status for one or more features](actions/get-feature-stale.md) | `GET /stale-features` | [docs](https://docs.growthbook.io/api) |
| [Get a Data Source's Information Schema](actions/get-information-schema.md) | `GET /data-sources/:dataSourceId/information-schema` | [docs](https://docs.growthbook.io/api) |
| [Get a single Information Schema Table by id](actions/get-information-schema-table.md) | `GET /information-schema-tables/:tableId` | [docs](https://docs.growthbook.io/api) |
| [Get a single metric](actions/get-metric.md) | `GET /metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single metricGroup](actions/get-metric-group.md) | `GET /metric-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Get metric usage across experiments](actions/get-metric-usage.md) | `GET /usage/metrics` | [docs](https://docs.growthbook.io/api) |
| [Get a single project](actions/get-project.md) | `GET /projects/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single query](actions/get-query.md) | `GET /queries/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single rampSchedule](actions/get-ramp-schedule.md) | `GET /ramp-schedules/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single rampScheduleTemplate](actions/get-ramp-schedule-template.md) | `GET /ramp-schedule-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single saved group](actions/get-saved-group.md) | `GET /saved-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single sdk connection](actions/get-sdk-connection.md) | `GET /sdk-connections/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a SDK payload](actions/get-sdk-payload.md) | `GET /sdk-payload/:key` | [docs](https://docs.growthbook.io/api) |
| [Get a single segment](actions/get-segment.md) | `GET /segments/:id` | [docs](https://docs.growthbook.io/api) |
| [Get organization settings](actions/get-settings.md) | `GET /settings` | [docs](https://docs.growthbook.io/api) |
| [Get a single team](actions/get-team.md) | `GET /teams/:id` | [docs](https://docs.growthbook.io/api) |
| [Get a single visual changeset](actions/get-visual-changeset.md) | `GET /visual-changesets/:id` | [docs](https://docs.growthbook.io/api) |
| [Jump to a specific step](actions/jump-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/jump` | [docs](https://docs.growthbook.io/api) |
| [Get the organization's archetypes](actions/list-archetypes.md) | `GET /archetypes` | [docs](https://docs.growthbook.io/api) |
| [Get the organization's attributes](actions/list-attributes.md) | `GET /attributes` | [docs](https://docs.growthbook.io/api) |
| [Get list of all code references for the current organization](actions/list-code-refs.md) | `GET /code-refs` | [docs](https://docs.growthbook.io/api) |
| [Get all custom fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://docs.growthbook.io/api) |
| [Get all dashboards](actions/list-dashboards.md) | `GET /dashboards` | [docs](https://docs.growthbook.io/api) |
| [Get all data sources](actions/list-data-sources.md) | `GET /data-sources` | [docs](https://docs.growthbook.io/api) |
| [Get all dimensions](actions/list-dimensions.md) | `GET /dimensions` | [docs](https://docs.growthbook.io/api) |
| [Get the organization's environments](actions/list-environments.md) | `GET /environments` | [docs](https://docs.growthbook.io/api) |
| [Get all experimentTemplates](actions/list-experiment-templates.md) | `GET /experiment-templates` | [docs](https://docs.growthbook.io/api) |
| [Get all experiments](actions/list-experiments.md) | `GET /experiments` | [docs](https://docs.growthbook.io/api) |
| [Get all fact metrics](actions/list-fact-metrics.md) | `GET /fact-metrics` | [docs](https://docs.growthbook.io/api) |
| [Get all filters for a fact table](actions/list-fact-table-filters.md) | `GET /fact-tables/:factTableId/filters` | [docs](https://docs.growthbook.io/api) |
| [Get all fact tables](actions/list-fact-tables.md) | `GET /fact-tables` | [docs](https://docs.growthbook.io/api) |
| [Get all features](actions/list-features.md) | `GET /features` | [docs](https://docs.growthbook.io/api) |
| [Get all organization members](actions/list-members.md) | `GET /members` | [docs](https://docs.growthbook.io/api) |
| [Get all metricGroups](actions/list-metric-groups.md) | `GET /metric-groups` | [docs](https://docs.growthbook.io/api) |
| [Get all metrics](actions/list-metrics.md) | `GET /metrics` | [docs](https://docs.growthbook.io/api) |
| [Get all organizations (only for super admins on multi-org Enterprise Plan only)](actions/list-organizations.md) | `GET /organizations` | [docs](https://docs.growthbook.io/api) |
| [Get all projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.growthbook.io/api) |
| [Get all rampScheduleTemplates](actions/list-ramp-schedule-templates.md) | `GET /ramp-schedule-templates` | [docs](https://docs.growthbook.io/api) |
| [Get all rampSchedules](actions/list-ramp-schedules.md) | `GET /ramp-schedules` | [docs](https://docs.growthbook.io/api) |
| [List feature revisions](actions/list-revisions.md) | `GET /revisions` | [docs](https://docs.growthbook.io/api) |
| [Get all saved group](actions/list-saved-groups.md) | `GET /saved-groups` | [docs](https://docs.growthbook.io/api) |
| [Get all sdk connections](actions/list-sdk-connections.md) | `GET /sdk-connections` | [docs](https://docs.growthbook.io/api) |
| [Get all segments](actions/list-segments.md) | `GET /segments` | [docs](https://docs.growthbook.io/api) |
| [Get all teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.growthbook.io/api) |
| [Get all visual changesets](actions/list-visual-changesets.md) | `GET /experiments/:id/visual-changesets` | [docs](https://docs.growthbook.io/api) |
| [Find a single sdk connection by its key](actions/lookup-sdk-connection-by-key.md) | `GET /sdk-connections/lookup/:key` | [docs](https://docs.growthbook.io/api) |
| [Pause a ramp schedule](actions/pause-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/pause` | [docs](https://docs.growthbook.io/api) |
| [Create a single archetype](actions/post-archetype.md) | `POST /archetypes` | [docs](https://docs.growthbook.io/api) |
| [Create a new attribute](actions/post-attribute.md) | `POST /attributes` | [docs](https://docs.growthbook.io/api) |
| [Bulk import fact tables, filters, and metrics](actions/post-bulk-import-facts.md) | `POST /bulk-import/facts` | [docs](https://docs.growthbook.io/api) |
| [Submit list of code references](actions/post-code-refs.md) | `POST /code-refs` | [docs](https://docs.growthbook.io/api) |
| [Postcopytransform](actions/post-copy-transform.md) | `POST /transform-copy` | [docs](https://docs.growthbook.io/api) |
| [Create a Data Source based visualization](actions/post-data-source-exploration.md) | `POST /product-analytics/data-source-exploration` | [docs](https://docs.growthbook.io/api) |
| [Create a single dimension](actions/post-dimension.md) | `POST /dimensions` | [docs](https://docs.growthbook.io/api) |
| [Create a new environment](actions/post-environment.md) | `POST /environments` | [docs](https://docs.growthbook.io/api) |
| [Create a single experiment](actions/post-experiment.md) | `POST /experiments` | [docs](https://docs.growthbook.io/api) |
| [Create Experiment Snapshot](actions/post-experiment-snapshot.md) | `POST /experiments/:id/snapshot` | [docs](https://docs.growthbook.io/api) |
| [Create a single fact metric](actions/post-fact-metric.md) | `POST /fact-metrics` | [docs](https://docs.growthbook.io/api) |
| [Create a fact metric analysis](actions/post-fact-metric-analysis.md) | `POST /fact-metrics/:id/analysis` | [docs](https://docs.growthbook.io/api) |
| [Create a single fact table](actions/post-fact-table.md) | `POST /fact-tables` | [docs](https://docs.growthbook.io/api) |
| [Run a Fact Table based visualization](actions/post-fact-table-exploration.md) | `POST /product-analytics/fact-table-exploration` | [docs](https://docs.growthbook.io/api) |
| [Create a single fact table filter](actions/post-fact-table-filter.md) | `POST /fact-tables/:factTableId/filters` | [docs](https://docs.growthbook.io/api) |
| [Create a single feature](actions/post-feature.md) | `POST /features` | [docs](https://docs.growthbook.io/api) |
| [Create a draft revision](actions/post-feature-revision.md) | `POST /features/:id/revisions` | [docs](https://docs.growthbook.io/api) |
| [Discard a draft revision](actions/post-feature-revision-discard.md) | `POST /features/:id/revisions/:version/discard` | [docs](https://docs.growthbook.io/api) |
| [Publish a draft revision](actions/post-feature-revision-publish.md) | `POST /features/:id/revisions/:version/publish` | [docs](https://docs.growthbook.io/api) |
| [Rebase a draft revision onto the current live version](actions/post-feature-revision-rebase.md) | `POST /features/:id/revisions/:version/rebase` | [docs](https://docs.growthbook.io/api) |
| [Request review for a draft revision](actions/post-feature-revision-request-review.md) | `POST /features/:id/revisions/:version/request-review` | [docs](https://docs.growthbook.io/api) |
| [Revert the feature to a prior revision](actions/post-feature-revision-revert.md) | `POST /features/:id/revisions/:version/revert` | [docs](https://docs.growthbook.io/api) |
| [Add a rule to a draft revision](actions/post-feature-revision-rule-add.md) | `POST /features/:id/revisions/:version/rules` | [docs](https://docs.growthbook.io/api) |
| [Reorder rules in an environment](actions/post-feature-revision-rules-reorder.md) | `POST /features/:id/revisions/:version/rules/reorder` | [docs](https://docs.growthbook.io/api) |
| [Submit a review on a draft revision](actions/post-feature-revision-submit-review.md) | `POST /features/:id/revisions/:version/submit-review` | [docs](https://docs.growthbook.io/api) |
| [Toggle an environment on/off in a draft revision](actions/post-feature-revision-toggle.md) | `POST /features/:id/revisions/:version/toggle` | [docs](https://docs.growthbook.io/api) |
| [Create a single metric](actions/post-metric.md) | `POST /metrics` | [docs](https://docs.growthbook.io/api) |
| [Create a Metric based visualization](actions/post-metric-exploration.md) | `POST /product-analytics/metric-exploration` | [docs](https://docs.growthbook.io/api) |
| [Create a single organization (only for super admins on multi-org Enterprise Plan only)](actions/post-organization.md) | `POST /organizations` | [docs](https://docs.growthbook.io/api) |
| [Create a single project](actions/post-project.md) | `POST /projects` | [docs](https://docs.growthbook.io/api) |
| [Create a single saved group](actions/post-saved-group.md) | `POST /saved-groups` | [docs](https://docs.growthbook.io/api) |
| [Create a single sdk connection](actions/post-sdk-connection.md) | `POST /sdk-connections` | [docs](https://docs.growthbook.io/api) |
| [Create a single segment](actions/post-segment.md) | `POST /segments` | [docs](https://docs.growthbook.io/api) |
| [Upload a variation screenshot](actions/post-variation-image-upload.md) | `POST /experiments/:id/variation/:variationId/screenshot/upload` | [docs](https://docs.growthbook.io/api) |
| [Create a visual change for a visual changeset](actions/post-visual-change.md) | `POST /visual-changesets/:id/visual-change` | [docs](https://docs.growthbook.io/api) |
| [Create a visual changeset for an experiment](actions/post-visual-changesets.md) | `POST /experiments/:id/visual-changesets` | [docs](https://docs.growthbook.io/api) |
| [Update a single archetype](actions/put-archetype.md) | `PUT /archetypes/:id` | [docs](https://docs.growthbook.io/api) |
| [Update an attribute](actions/put-attribute.md) | `PUT /attributes/:property` | [docs](https://docs.growthbook.io/api) |
| [Update an environment](actions/put-environment.md) | `PUT /environments/:id` | [docs](https://docs.growthbook.io/api) |
| [Set archived state in a draft revision](actions/put-feature-revision-archive.md) | `PUT /features/:id/revisions/:version/archive` | [docs](https://docs.growthbook.io/api) |
| [Set the default value in a draft revision](actions/put-feature-revision-default-value.md) | `PUT /features/:id/revisions/:version/default-value` | [docs](https://docs.growthbook.io/api) |
| [Set holdout in a draft revision](actions/put-feature-revision-holdout.md) | `PUT /features/:id/revisions/:version/holdout` | [docs](https://docs.growthbook.io/api) |
| [Update revision metadata (comment, title, feature metadata)](actions/put-feature-revision-metadata.md) | `PUT /features/:id/revisions/:version/metadata` | [docs](https://docs.growthbook.io/api) |
| [Set feature-level prerequisites in a draft revision](actions/put-feature-revision-prerequisites.md) | `PUT /features/:id/revisions/:version/prerequisites` | [docs](https://docs.growthbook.io/api) |
| [Update a rule in a draft revision](actions/put-feature-revision-rule.md) | `PUT /features/:id/revisions/:version/rules/:ruleId` | [docs](https://docs.growthbook.io/api) |
| [Set ramp schedule for a rule](actions/put-feature-revision-rule-ramp-schedule.md) | `PUT /features/:id/revisions/:version/rules/:ruleId/ramp-schedule` | [docs](https://docs.growthbook.io/api) |
| [Update a metric](actions/put-metric.md) | `PUT /metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Edit a single organization (only for super admins on multi-org Enterprise Plan only)](actions/put-organization.md) | `PUT /organizations/:id` | [docs](https://docs.growthbook.io/api) |
| [Edit a single project](actions/put-project.md) | `PUT /projects/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single sdk connection](actions/put-sdk-connection.md) | `PUT /sdk-connections/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a visual change for a visual changeset](actions/put-visual-change.md) | `PUT /visual-changesets/:id/visual-change/:visualChangeId` | [docs](https://docs.growthbook.io/api) |
| [Update a visual changeset](actions/put-visual-changeset.md) | `PUT /visual-changesets/:id` | [docs](https://docs.growthbook.io/api) |
| [Remove members from team](actions/remove-team-member.md) | `DELETE /teams/:id/members` | [docs](https://docs.growthbook.io/api) |
| [Resume a paused ramp schedule](actions/resume-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/resume` | [docs](https://docs.growthbook.io/api) |
| [Revert a feature to a specific revision](actions/revert-feature.md) | `POST /features/:id/revert` | [docs](https://docs.growthbook.io/api) |
| [Roll back a ramp schedule](actions/rollback-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/rollback` | [docs](https://docs.growthbook.io/api) |
| [Start a ramp schedule](actions/start-ramp-schedule.md) | `POST /ramp-schedules/:id/actions/start` | [docs](https://docs.growthbook.io/api) |
| [Toggle a feature in one or more environments](actions/toggle-feature.md) | `POST /features/:id/toggle` | [docs](https://docs.growthbook.io/api) |
| [Update a single customField](actions/update-custom-field.md) | `PUT /custom-fields/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single dashboard](actions/update-dashboard.md) | `PUT /dashboards/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single dimension](actions/update-dimension.md) | `POST /dimensions/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single experiment](actions/update-experiment.md) | `POST /experiments/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single experimentTemplate](actions/update-experiment-template.md) | `PUT /experiment-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single fact metric](actions/update-fact-metric.md) | `POST /fact-metrics/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single fact table](actions/update-fact-table.md) | `POST /fact-tables/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single fact table filter](actions/update-fact-table-filter.md) | `POST /fact-tables/:factTableId/filters/:id` | [docs](https://docs.growthbook.io/api) |
| [Partially update a feature](actions/update-feature.md) | `POST /features/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a member's global role (including any enviroment restrictions, if applicable). Can also update a member's project roles if your plan supports it.](actions/update-member-role.md) | `POST /members/:id/role` | [docs](https://docs.growthbook.io/api) |
| [Update a single metricGroup](actions/update-metric-group.md) | `PUT /metric-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single rampSchedule](actions/update-ramp-schedule.md) | `PUT /ramp-schedules/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single rampScheduleTemplate](actions/update-ramp-schedule-template.md) | `PUT /ramp-schedule-templates/:id` | [docs](https://docs.growthbook.io/api) |
| [Partially update a single saved group](actions/update-saved-group.md) | `POST /saved-groups/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single segment](actions/update-segment.md) | `POST /segments/:id` | [docs](https://docs.growthbook.io/api) |
| [Update a single team](actions/update-team.md) | `PUT /teams/:id` | [docs](https://docs.growthbook.io/api) |
