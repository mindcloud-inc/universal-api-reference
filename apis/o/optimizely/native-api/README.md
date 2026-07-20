# Optimizely: Native API Reference

A consolidated summary of Optimizely's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://docs.developers.optimizely.com/web-experimentation/reference/overview
- **OpenAPI specification:** https://api.optimizely.com/v2/swagger.json
- **API base URL:** `https://api.optimizely.com/v2`

## Authentication

### Personal Access Token

Use an Optimizely personal access token. Optimizely sends this token as Authorization: Bearer <token> on every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.developers.optimizely.com/web-experimentation/docs/personal-access-token)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Attribute](actions/get-attribute.md) | `GET /attributes/{attributeId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_attribute) |
| [Get Audience](actions/get-audience.md) | `GET /audiences/{audienceId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_audience) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{campaignId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_campaign) |
| [Get Campaign Results](actions/get-campaign-results.md) | `GET /campaigns/{campaignId}/results` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_campaign_results) |
| [Get Environment](actions/get-environment.md) | `GET /environments/{environmentId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_environment) |
| [Get Environment Datafile](actions/get-environment-datafile.md) | `GET /environments/{environmentId}/datafile` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_datafile) |
| [Get Event](actions/get-event.md) | `GET /events/{eventId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_event) |
| [Get Experiment](actions/get-experiment.md) | `GET /experiments/{experimentId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment) |
| [Get Experiment Results](actions/get-experiment-results.md) | `GET /experiments/{experimentId}/results` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_results) |
| [Get Experiment Timeseries](actions/get-experiment-timeseries.md) | `GET /experiments/{experimentId}/timeseries` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_timeseries) |
| [Get Extension](actions/get-extension.md) | `GET /extensions/{extensionId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_extension) |
| [Get Feature](actions/get-feature.md) | `GET /features/{featureId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_feature) |
| [Get Group](actions/get-group.md) | `GET /groups/{groupId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_group) |
| [Get Page](actions/get-page.md) | `GET /pages/{pageId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_page) |
| [Get Plan](actions/get-plan.md) | `GET /plan` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_plan) |
| [Get Project](actions/get-project.md) | `GET /projects/{projectId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_project) |
| [Get Section](actions/get-section.md) | `GET /experiments/{experimentId}/sections/{sectionId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_section) |
| [Get Subject Access Request](actions/get-subject-access-request.md) | `GET /subject-access-requests/{requestId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_sar_request) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhookId}` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_webhook) |
| [List Attributes](actions/list-attributes.md) | `GET /attributes` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_attributes) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_audiences) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_campaigns) |
| [List Changes](actions/list-changes.md) | `GET /changes` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_change_history) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_environments) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_events) |
| [List Experiments](actions/list-experiments.md) | `GET /experiments` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_experiments) |
| [List Extensions](actions/list-extensions.md) | `GET /extensions` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_extensions) |
| [List Features](actions/list-features.md) | `GET /features` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_features) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_groups) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_pages) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_projects) |
| [List Sections](actions/list-sections.md) | `GET /experiments/{experimentId}/sections` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_sections) |
| [List Subject Access Requests](actions/list-subject-access-requests.md) | `GET /subject-access-requests` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_sar_requests_by_account) |
| [List Webhooks](actions/list-webhooks.md) | `GET /projects/{projectId}/webhooks` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/list_webhooks) |
| [Search Entities](actions/search-entities.md) | `GET /search` | [docs](https://docs.developers.optimizely.com/web-experimentation/reference/get_search_results) |
