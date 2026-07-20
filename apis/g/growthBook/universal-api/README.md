# <img src="https://images.mindcloud.co/apps/icons/growthbook-icon_1776455736610.png" alt="GrowthBook logo" width="28" height="28"> GrowthBook: Universal API

GrowthBook is an open-source feature flagging and experimentation platform with a REST API for managing projects, features, experiments, metrics, environments, SDK connections, and related configuration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/growthBook/latest
- **Category:** IT Operations / DevOps
- **Actions:** 179
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.growthbook.io
- **Vendor API docs:** https://docs.growthbook.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (179)

### Analyticsexploration

| Action | Method | Description |
| --- | --- | --- |
| [Create a Data Source based visualization](actions/post-data-source-exploration.md) | POST | Creates a data source visualization in GrowthBook. |
| [Run a Fact Table based visualization](actions/post-fact-table-exploration.md) | POST | Runs a fact table visualization in GrowthBook. |
| [Create a Metric based visualization](actions/post-metric-exploration.md) | POST | Creates a metric-based visualization in GrowthBook. |

### Archetype

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single archetype](actions/delete-archetype.md) | DELETE | Deletes an existing archetype from GrowthBook. |
| [Get a single archetype](actions/get-archetype.md) | GET | Retrieves an archetype from your GrowthBook organization. |
| [Get the organization's archetypes](actions/list-archetypes.md) | GET | Retrieves the organization's archetypes from GrowthBook. |
| [Create a single archetype](actions/post-archetype.md) | POST | Creates a new archetype in GrowthBook. |
| [Update a single archetype](actions/put-archetype.md) | PUT | Updates an existing archetype in GrowthBook. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single attribute](actions/delete-attribute.md) | DELETE | Deletes an existing attribute from GrowthBook. |
| [Get the organization's attributes](actions/list-attributes.md) | GET | Retrieves the organization's attributes from GrowthBook. |
| [Create a new attribute](actions/post-attribute.md) | POST | Creates a new attribute in GrowthBook. |
| [Update an attribute](actions/put-attribute.md) | PUT | Updates an existing attribute in GrowthBook. |

### Code Reference

| Action | Method | Description |
| --- | --- | --- |
| [Get list of code references for a single feature id](actions/get-code-refs.md) | GET | Retrieves code references for a GrowthBook feature. |
| [Get list of all code references for the current organization](actions/list-code-refs.md) | GET | Retrieves code references from your GrowthBook organization. |
| [Submit list of code references](actions/post-code-refs.md) | POST | Submits code references to your GrowthBook organization. |

### Customfield

| Action | Method | Description |
| --- | --- | --- |
| [Create a single customField](actions/create-custom-field.md) | POST | Creates a new custom field in GrowthBook. |
| [Delete a single customField](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from GrowthBook. |
| [Get a single customField](actions/get-custom-field.md) | GET | Retrieves a custom field from your GrowthBook organization. |
| [Get all custom fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from your GrowthBook organization. |
| [Update a single customField](actions/update-custom-field.md) | PUT | Updates an existing custom field in GrowthBook. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Create a single dashboard](actions/create-dashboard.md) | POST | Creates a new dashboard in GrowthBook. |
| [Delete a single dashboard](actions/delete-dashboard.md) | DELETE | Deletes an existing dashboard from GrowthBook. |
| [Get a single dashboard](actions/get-dashboard.md) | GET | Retrieves a dashboard from your GrowthBook organization. |
| [Get all dashboards for an experiment](actions/get-dashboards-for-experiment.md) | GET | Retrieves dashboards for a GrowthBook experiment. |
| [Get all dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from your GrowthBook organization. |
| [Update a single dashboard](actions/update-dashboard.md) | PUT | Updates an existing dashboard in GrowthBook. |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Get a single data source](actions/get-data-source.md) | GET | Retrieves a data source from your GrowthBook organization. |
| [Get a Data Source's Information Schema](actions/get-information-schema.md) | GET | Retrieves a data source information schema from GrowthBook. |
| [Get a single Information Schema Table by id](actions/get-information-schema-table.md) | GET | Retrieves an information schema table from GrowthBook. |
| [Get all data sources](actions/list-data-sources.md) | GET | Retrieves data sources from your GrowthBook organization. |

### Dimension

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single dimension](actions/delete-dimension.md) | DELETE | Deletes an existing dimension from GrowthBook. |
| [Get a single dimension](actions/get-dimension.md) | GET | Retrieves a dimension from your GrowthBook organization. |
| [Get all dimensions](actions/list-dimensions.md) | GET | Retrieves dimensions from your GrowthBook organization. |
| [Create a single dimension](actions/post-dimension.md) | POST | Creates a new dimension in GrowthBook. |
| [Update a single dimension](actions/update-dimension.md) | PUT | Updates an existing dimension in GrowthBook. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from GrowthBook. |
| [Get the organization's environments](actions/list-environments.md) | GET | Retrieves the organization's environments from GrowthBook. |
| [Create a new environment](actions/post-environment.md) | POST | Creates a new environment in GrowthBook. |
| [Update an environment](actions/put-environment.md) | PUT | Updates an existing environment in GrowthBook. |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Delete a variation screenshot](actions/delete-variation-screenshot.md) | DELETE | Deletes a variation screenshot from GrowthBook. |
| [Get a single experiment](actions/get-experiment.md) | GET | Retrieves an experiment from your GrowthBook organization. |
| [Get a list of experiments with names and ids](actions/get-experiment-names.md) | GET | Retrieves experiment names and IDs from GrowthBook. |
| [Get results for an experiment](actions/get-experiment-results.md) | GET | Retrieves results for a GrowthBook experiment. |
| [Get all experiments](actions/list-experiments.md) | GET | Retrieves experiments from your GrowthBook organization. |
| [Create a single experiment](actions/post-experiment.md) | POST | Creates a new experiment in GrowthBook. |
| [Create Experiment Snapshot](actions/post-experiment-snapshot.md) | POST | Creates an experiment snapshot in GrowthBook. |
| [Upload a variation screenshot](actions/post-variation-image-upload.md) | POST | Uploads a variation screenshot to GrowthBook. |
| [Update a single experiment](actions/update-experiment.md) | PUT | Updates an existing experiment in GrowthBook. |

### Experimenttemplate

| Action | Method | Description |
| --- | --- | --- |
| [Bulk create or update experiment templates](actions/bulk-import-experiment-templates.md) | POST | Bulk creates or updates experiment templates in GrowthBook. |
| [Create a single experimentTemplate](actions/create-experiment-template.md) | POST | Creates a new experiment template in GrowthBook. |
| [Delete a single experimentTemplate](actions/delete-experiment-template.md) | DELETE | Deletes an existing experiment template from GrowthBook. |
| [Get a single experimentTemplate](actions/get-experiment-template.md) | GET | Retrieves an experiment template from your GrowthBook organization. |
| [Get all experimentTemplates](actions/list-experiment-templates.md) | GET | Retrieves experimenttemplates from your GrowthBook organization. |
| [Update a single experimentTemplate](actions/update-experiment-template.md) | PUT | Updates an existing experiment template in GrowthBook. |

### Fact Metric

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single fact metric](actions/delete-fact-metric.md) | DELETE | Deletes an existing fact metric from GrowthBook. |
| [Get a single fact metric](actions/get-fact-metric.md) | GET | Retrieves a fact metric from your GrowthBook organization. |
| [Get all fact metrics](actions/list-fact-metrics.md) | GET | Retrieves fact metrics from your GrowthBook organization. |
| [Create a single fact metric](actions/post-fact-metric.md) | POST | Creates a new fact metric in GrowthBook. |
| [Create a fact metric analysis](actions/post-fact-metric-analysis.md) | POST | Creates a fact metric analysis in GrowthBook. |
| [Update a single fact metric](actions/update-fact-metric.md) | POST | Updates an existing fact metric in GrowthBook. |

### Fact Table

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single fact table](actions/delete-fact-table.md) | DELETE | Deletes an existing fact table from GrowthBook. |
| [Deletes a single fact table filter](actions/delete-fact-table-filter.md) | DELETE | Deletes a fact table filter from GrowthBook. |
| [Get a single fact table](actions/get-fact-table.md) | GET | Retrieves a fact table from your GrowthBook organization. |
| [Get a single fact filter](actions/get-fact-table-filter.md) | GET | Retrieves a fact table filter from GrowthBook. |
| [Get all filters for a fact table](actions/list-fact-table-filters.md) | GET | Retrieves filters for a GrowthBook fact table. |
| [Get all fact tables](actions/list-fact-tables.md) | GET | Retrieves fact tables from your GrowthBook organization. |
| [Bulk import fact tables, filters, and metrics](actions/post-bulk-import-facts.md) | POST | Bulk imports fact tables, filters, and metrics into GrowthBook. |
| [Create a single fact table](actions/post-fact-table.md) | POST | Creates a new fact table in GrowthBook. |
| [Create a single fact table filter](actions/post-fact-table-filter.md) | POST | Creates a fact table filter in GrowthBook. |
| [Update a single fact table](actions/update-fact-table.md) | PUT | Updates an existing fact table in GrowthBook. |
| [Update a single fact table filter](actions/update-fact-table-filter.md) | POST | Updates a fact table filter in GrowthBook. |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single feature](actions/delete-feature.md) | DELETE | Deletes an existing feature from GrowthBook. |
| [Get a single feature](actions/get-feature.md) | GET | Retrieves a feature from your GrowthBook organization. |
| [Get list of feature keys](actions/get-feature-keys.md) | GET | Retrieves feature keys from your GrowthBook organization. |
| [Get stale status for one or more features](actions/get-feature-stale.md) | GET | Retrieves stale status for GrowthBook features. |
| [Get all features](actions/list-features.md) | GET | Retrieves features from your GrowthBook organization. |
| [Create a single feature](actions/post-feature.md) | POST | Creates a new feature in GrowthBook. |
| [Revert a feature to a specific revision](actions/revert-feature.md) | PUT | Reverts a feature to a specific GrowthBook revision. |
| [Toggle a feature in one or more environments](actions/toggle-feature.md) | PUT | Toggles a feature in GrowthBook environments. |
| [Partially update a feature](actions/update-feature.md) | PUT | Updates an existing feature in GrowthBook. |

### Feature Revision

| Action | Method | Description |
| --- | --- | --- |
| [Delete a rule from a draft revision](actions/delete-feature-revision-rule.md) | DELETE | Deletes a rule from a GrowthBook feature revision. |
| [Remove ramp schedule from a rule](actions/delete-feature-revision-rule-ramp-schedule.md) | DELETE | Removes a ramp schedule from a GrowthBook rule. |
| [Get a single feature revision](actions/get-feature-revision.md) | GET | Retrieves a feature revision from your GrowthBook organization. |
| [Get the most recent active draft revision](actions/get-feature-revision-latest.md) | GET | Retrieves the latest draft feature revision from GrowthBook. |
| [Get merge status for a draft revision](actions/get-feature-revision-merge-status.md) | GET | Retrieves merge status for a GrowthBook draft revision. |
| [List revisions for a feature](actions/get-feature-revisions.md) | GET | Retrieves revisions for a GrowthBook feature. |
| [List feature revisions](actions/list-revisions.md) | GET | Retrieves feature revisions from your GrowthBook organization. |
| [Create a draft revision](actions/post-feature-revision.md) | POST | Creates a draft feature revision in GrowthBook. |
| [Discard a draft revision](actions/post-feature-revision-discard.md) | PUT | Discards a draft feature revision in GrowthBook. |
| [Publish a draft revision](actions/post-feature-revision-publish.md) | PUT | Publishes a draft feature revision in GrowthBook. |
| [Rebase a draft revision onto the current live version](actions/post-feature-revision-rebase.md) | PUT | Rebases a draft feature revision in GrowthBook. |
| [Request review for a draft revision](actions/post-feature-revision-request-review.md) | POST | Requests review for a GrowthBook draft revision. |
| [Revert the feature to a prior revision](actions/post-feature-revision-revert.md) | PUT | Reverts a GrowthBook feature to a prior revision. |
| [Add a rule to a draft revision](actions/post-feature-revision-rule-add.md) | POST | Adds a rule to a GrowthBook feature revision. |
| [Reorder rules in an environment](actions/post-feature-revision-rules-reorder.md) | PUT | Reorders rules in a GrowthBook feature revision. |
| [Submit a review on a draft revision](actions/post-feature-revision-submit-review.md) | POST | Submits a review for a GrowthBook draft revision. |
| [Toggle an environment on/off in a draft revision](actions/post-feature-revision-toggle.md) | PUT | Toggles an environment in a GrowthBook feature revision. |
| [Set archived state in a draft revision](actions/put-feature-revision-archive.md) | PUT | Sets archived state for a GrowthBook feature revision. |
| [Set the default value in a draft revision](actions/put-feature-revision-default-value.md) | PUT | Sets the default value for a GrowthBook feature revision. |
| [Set holdout in a draft revision](actions/put-feature-revision-holdout.md) | PUT | Sets holdout for a GrowthBook feature revision. |
| [Update revision metadata (comment, title, feature metadata)](actions/put-feature-revision-metadata.md) | PUT | Updates metadata for a GrowthBook feature revision. |
| [Set feature-level prerequisites in a draft revision](actions/put-feature-revision-prerequisites.md) | PUT | Sets prerequisites for a GrowthBook feature revision. |
| [Update a rule in a draft revision](actions/put-feature-revision-rule.md) | PUT | Updates a rule in a GrowthBook feature revision. |
| [Set ramp schedule for a rule](actions/put-feature-revision-rule-ramp-schedule.md) | PUT | Sets a ramp schedule for a GrowthBook rule. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Removes a single user from an organization](actions/delete-member.md) | DELETE | Removes a member from your GrowthBook organization. |
| [Get all organization members](actions/list-members.md) | GET | Retrieves organization members from your GrowthBook organization. |
| [Update a member's global role (including any enviroment restrictions, if applicable). Can also update a member's project roles if your plan supports it.](actions/update-member-role.md) | PUT | Updates a member role in GrowthBook. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a metric](actions/delete-metric.md) | DELETE | Deletes an existing metric from GrowthBook. |
| [Get a single metric](actions/get-metric.md) | GET | Retrieves a metric from your GrowthBook organization. |
| [Get all metrics](actions/list-metrics.md) | GET | Retrieves metrics from your GrowthBook organization. |
| [Create a single metric](actions/post-metric.md) | POST | Creates a new metric in GrowthBook. |
| [Update a metric](actions/put-metric.md) | PUT | Updates an existing metric in GrowthBook. |

### Metricgroup

| Action | Method | Description |
| --- | --- | --- |
| [Create a single metricGroup](actions/create-metric-group.md) | POST | Creates a new metric group in GrowthBook. |
| [Delete a single metricGroup](actions/delete-metric-group.md) | DELETE | Deletes an existing metric group from GrowthBook. |
| [Get a single metricGroup](actions/get-metric-group.md) | GET | Retrieves a metric group from your GrowthBook organization. |
| [Get all metricGroups](actions/list-metric-groups.md) | GET | Retrieves metricgroups from your GrowthBook organization. |
| [Update a single metricGroup](actions/update-metric-group.md) | PUT | Updates an existing metric group in GrowthBook. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get all organizations (only for super admins on multi-org Enterprise Plan only)](actions/list-organizations.md) | GET | Retrieves organizations from your GrowthBook account. |
| [Create a single organization (only for super admins on multi-org Enterprise Plan only)](actions/post-organization.md) | POST | Creates a new organization in GrowthBook. |
| [Edit a single organization (only for super admins on multi-org Enterprise Plan only)](actions/put-organization.md) | PUT | Updates an existing organization in GrowthBook. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single project](actions/delete-project.md) | DELETE | Deletes an existing project from GrowthBook. |
| [Get a single project](actions/get-project.md) | GET | Retrieves a project from your GrowthBook organization. |
| [Get all projects](actions/list-projects.md) | GET | Retrieves projects from your GrowthBook organization. |
| [Create a single project](actions/post-project.md) | POST | Creates a new project in GrowthBook. |
| [Edit a single project](actions/put-project.md) | PUT | Updates an existing project in GrowthBook. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Get a single query](actions/get-query.md) | GET | Retrieves a query from your GrowthBook organization. |

### Ramp Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Add a target rule to a ramp schedule](actions/add-target-ramp-schedule.md) | POST | Adds a target rule to a GrowthBook ramp schedule. |
| [Approve the current pending-approval step](actions/approve-step-ramp-schedule.md) | POST | Approves the current step in a GrowthBook ramp schedule. |
| [Complete a ramp schedule immediately](actions/complete-ramp-schedule.md) | POST | Completes a GrowthBook ramp schedule immediately. |
| [Create a single rampSchedule](actions/create-ramp-schedule.md) | POST | Creates a new ramp schedule in GrowthBook. |
| [Delete a single rampSchedule](actions/delete-ramp-schedule.md) | DELETE | Deletes an existing ramp schedule from GrowthBook. |
| [Remove a target rule from a ramp schedule](actions/eject-target-ramp-schedule.md) | POST | Removes a target rule from a GrowthBook ramp schedule. |
| [Get a single rampSchedule](actions/get-ramp-schedule.md) | GET | Retrieves a ramp schedule from your GrowthBook organization. |
| [Jump to a specific step](actions/jump-ramp-schedule.md) | POST | Jumps to a specific step in a GrowthBook ramp schedule. |
| [Get all rampSchedules](actions/list-ramp-schedules.md) | GET | Retrieves ramp schedules from your GrowthBook organization. |
| [Pause a ramp schedule](actions/pause-ramp-schedule.md) | POST | Pauses a ramp schedule in GrowthBook. |
| [Resume a paused ramp schedule](actions/resume-ramp-schedule.md) | POST | Resumes a ramp schedule in GrowthBook. |
| [Roll back a ramp schedule](actions/rollback-ramp-schedule.md) | POST | Rolls back a ramp schedule in GrowthBook. |
| [Start a ramp schedule](actions/start-ramp-schedule.md) | POST | Starts a ramp schedule in GrowthBook. |
| [Update a single rampSchedule](actions/update-ramp-schedule.md) | PUT | Updates an existing ramp schedule in GrowthBook. |

### Rampscheduletemplate

| Action | Method | Description |
| --- | --- | --- |
| [Create a single rampScheduleTemplate](actions/create-ramp-schedule-template.md) | POST | Creates a new ramp schedule template in GrowthBook. |
| [Delete a single rampScheduleTemplate](actions/delete-ramp-schedule-template.md) | DELETE | Deletes an existing ramp schedule template from GrowthBook. |
| [Get a single rampScheduleTemplate](actions/get-ramp-schedule-template.md) | GET | Retrieves a ramp schedule template from your GrowthBook organization. |
| [Get all rampScheduleTemplates](actions/list-ramp-schedule-templates.md) | GET | Retrieves rampscheduletemplates from your GrowthBook organization. |
| [Update a single rampScheduleTemplate](actions/update-ramp-schedule-template.md) | PUT | Updates an existing ramp schedule template in GrowthBook. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get a SDK payload](actions/get-sdk-payload.md) | GET | Retrieves an SDK payload from GrowthBook. |
| [Postcopytransform](actions/post-copy-transform.md) | POST | Copies a transform in your GrowthBook organization. |

### Saved Group

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single saved group](actions/delete-saved-group.md) | DELETE | Deletes an existing saved group from GrowthBook. |
| [Get a single saved group](actions/get-saved-group.md) | GET | Retrieves a saved group from your GrowthBook organization. |
| [Get all saved group](actions/list-saved-groups.md) | GET | Retrieves saved groups from your GrowthBook organization. |
| [Create a single saved group](actions/post-saved-group.md) | POST | Creates a new saved group in GrowthBook. |
| [Partially update a single saved group](actions/update-saved-group.md) | PUT | Updates an existing saved group in GrowthBook. |

### Sdk Connection

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single SDK connection](actions/delete-sdk-connection.md) | DELETE | Deletes an existing SDK connection from GrowthBook. |
| [Get a single sdk connection](actions/get-sdk-connection.md) | GET | Retrieves a SDK connection from your GrowthBook organization. |
| [Get all sdk connections](actions/list-sdk-connections.md) | GET | Retrieves SDK connections from your GrowthBook organization. |
| [Find a single sdk connection by its key](actions/lookup-sdk-connection-by-key.md) | GET | Retrieves an SDK connection by key from GrowthBook. |
| [Create a single sdk connection](actions/post-sdk-connection.md) | POST | Creates a new SDK connection in GrowthBook. |
| [Update a single sdk connection](actions/put-sdk-connection.md) | PUT | Updates an existing SDK connection in GrowthBook. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Deletes a single segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from GrowthBook. |
| [Get a single segment](actions/get-segment.md) | GET | Retrieves a segment from your GrowthBook organization. |
| [Get all segments](actions/list-segments.md) | GET | Retrieves segments from your GrowthBook organization. |
| [Create a single segment](actions/post-segment.md) | POST | Creates a new segment in GrowthBook. |
| [Update a single segment](actions/update-segment.md) | PUT | Updates an existing segment in GrowthBook. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get organization settings](actions/get-settings.md) | GET | Retrieves organization settings from your GrowthBook account. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get an experiment snapshot status](actions/get-experiment-snapshot.md) | GET | Retrieves experiment snapshot status from GrowthBook. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Add members to team](actions/add-team-members.md) | POST | Adds members to a team in GrowthBook. |
| [Create a single team](actions/create-team.md) | POST | Creates a new team in GrowthBook. |
| [Delete a single team](actions/delete-team.md) | DELETE | Deletes an existing team from GrowthBook. |
| [Get a single team](actions/get-team.md) | GET | Retrieves a team from your GrowthBook organization. |
| [Get all teams](actions/list-teams.md) | GET | Retrieves teams from your GrowthBook organization. |
| [Remove members from team](actions/remove-team-member.md) | DELETE | Removes members from a team in GrowthBook. |
| [Update a single team](actions/update-team.md) | PUT | Updates an existing team in GrowthBook. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get metric usage across experiments](actions/get-metric-usage.md) | GET | Retrieves metric usage across GrowthBook experiments. |

### Visual Changeset

| Action | Method | Description |
| --- | --- | --- |
| [Get a single visual changeset](actions/get-visual-changeset.md) | GET | Retrieves a visual changeset from your GrowthBook organization. |
| [Get all visual changesets](actions/list-visual-changesets.md) | GET | Retrieves visual changesets for a GrowthBook experiment. |
| [Create a visual change for a visual changeset](actions/post-visual-change.md) | POST | Creates a visual change in a GrowthBook changeset. |
| [Create a visual changeset for an experiment](actions/post-visual-changesets.md) | POST | Creates a visual changeset for a GrowthBook experiment. |
| [Update a visual change for a visual changeset](actions/put-visual-change.md) | PUT | Updates a visual change in a GrowthBook changeset. |
| [Update a visual changeset](actions/put-visual-changeset.md) | PUT | Updates a visual changeset in your GrowthBook organization. |

