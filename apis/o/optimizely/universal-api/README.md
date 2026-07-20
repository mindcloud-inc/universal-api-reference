# <img src="https://images.mindcloud.co/apps/icons/optimizely-icon_1775482531456.png" alt="Optimizely logo" width="28" height="28"> Optimizely: Universal API

Use Optimizely Web Experimentation v2 to manage projects, campaigns, experiments, pages, audiences, events, attributes, extensions, groups, sections, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/optimizely/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.optimizely.com/
- **Vendor API docs:** https://docs.developers.optimizely.com/web-experimentation/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [Get Audience](actions/get-audience.md) | GET | Retrieves audience details from the Optimizely API. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves a list of audiences from Optimizely. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Changes](actions/list-changes.md) | GET | Retrieves project change history from the Optimizely API. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves campaign details from the Optimizely API. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Optimizely. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Attribute](actions/get-attribute.md) | GET | Retrieves attribute details from the Optimizely API. |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves a list of attributes from Optimizely. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment](actions/get-environment.md) | GET | Retrieves environment details from the Optimizely API. |
| [Get Environment Datafile](actions/get-environment-datafile.md) | GET | Retrieves an environment datafile from Optimizely. |
| [List Environments](actions/list-environments.md) | GET | Retrieves a list of environments from Optimizely. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves event details from the Optimizely API. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Optimizely. |

### Experiments

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment](actions/get-experiment.md) | GET | Retrieves experiment details from the Optimizely API. |
| [List Experiments](actions/list-experiments.md) | GET | Retrieves a list of experiments from Optimizely. |

### Feature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature](actions/get-feature.md) | GET | Retrieves feature details from the Optimizely API. |
| [List Features](actions/list-features.md) | GET | Retrieves a list of features from Optimizely. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves an exclusion group from Optimizely. |
| [List Groups](actions/list-groups.md) | GET | Retrieves exclusion groups from the Optimizely API. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Extension](actions/get-extension.md) | GET | Retrieves extension details from the Optimizely API. |
| [List Extensions](actions/list-extensions.md) | GET | Retrieves a list of extensions from Optimizely. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Section](actions/get-section.md) | GET | Retrieves a section from an Optimizely experiment. |
| [List Sections](actions/list-sections.md) | GET | Retrieves sections for an experiment in Optimizely. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves page details from the Optimizely API. |
| [List Pages](actions/list-pages.md) | GET | Retrieves a list of pages from Optimizely. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from the Optimizely API. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Optimizely. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Results](actions/get-campaign-results.md) | GET | Retrieves results for a campaign in Optimizely. |
| [Get Experiment Results](actions/get-experiment-results.md) | GET | Retrieves results for an experiment in Optimizely. |
| [Get Experiment Timeseries](actions/get-experiment-timeseries.md) | GET | Retrieves experiment time series from Optimizely. |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Subject Access Request](actions/get-subject-access-request.md) | GET | Retrieves a subject access request from Optimizely. |
| [List Subject Access Requests](actions/list-subject-access-requests.md) | GET | Retrieves subject access requests from Optimizely. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves plan and usage information from Optimizely. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Search Entities](actions/search-entities.md) | GET | Finds entities in Optimizely by search query. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook details from the Optimizely API. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks for a project in Optimizely. |

