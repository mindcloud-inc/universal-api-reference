# <img src="https://images.mindcloud.co/apps/icons/id9pdpn-muy-logos_1772045715796.jpeg" alt="Kadoa logo" width="28" height="28"> Kadoa: Universal API

Extract web data, run workflows, monitor sites, and manage schemas.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kadoa/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 44
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kadoa.com
- **Vendor API docs:** https://docs.kadoa.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Schemas](actions/list-schemas.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (44)

### Changes

| Action | Method | Description |
| --- | --- | --- |
| [Get Change](actions/get-change.md) | GET |  |
| [List Changes](actions/list-changes.md) | GET |  |

### Crawl Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawl Page Content](actions/get-crawl-page-content.md) | GET |  |
| [Get Crawl Pages](actions/get-crawl-pages.md) | GET |  |
| [Get Crawl Status](actions/get-crawl-status.md) | GET |  |
| [Start Crawl](actions/start-crawl.md) | POST |  |

### Event Types

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Type](actions/get-event-type.md) | GET |  |
| [List Event Types](actions/list-event-types.md) | GET |  |

### Extractions

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data](actions/extract-data.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Notification Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Notification Channel](actions/create-notification-channel.md) | POST |  |
| [Delete Notification Channel](actions/delete-notification-channel.md) | DELETE |  |
| [Get Notification Channel](actions/get-notification-channel.md) | GET |  |
| [List Notification Channels](actions/list-notification-channels.md) | GET |  |
| [Update Notification Channel](actions/update-notification-channel.md) | PUT |  |

### Notification Settings

| Action | Method | Description |
| --- | --- | --- |
| [Create Notification Settings](actions/create-notification-settings.md) | POST |  |
| [Delete Notification Settings](actions/delete-notification-settings.md) | DELETE |  |
| [Get Notification Settings](actions/get-notification-settings.md) | GET |  |
| [List Notification Settings](actions/list-notification-settings.md) | GET |  |
| [Update Notification Settings](actions/update-notification-settings.md) | PUT |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Test Notification](actions/test-notification.md) | POST |  |

### Schemas

| Action | Method | Description |
| --- | --- | --- |
| [Create Schema](actions/create-schema.md) | POST |  |
| [Delete Schema](actions/delete-schema.md) | DELETE |  |
| [Get Schema](actions/get-schema.md) | GET |  |
| [List Schemas](actions/list-schemas.md) | GET |  |
| [Update Schema](actions/update-schema.md) | PUT |  |

### Validation Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Config](actions/get-validation-config.md) | GET |  |
| [Toggle Validation](actions/toggle-validation.md) | PUT |  |

### Validation Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Results](actions/get-validation-results.md) | GET |  |

### Validation Rules

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Approve Rules](actions/bulk-approve-rules.md) | PUT |  |
| [Bulk Delete Rules](actions/bulk-delete-rules.md) | DELETE |  |
| [Generate Validation Rules](actions/generate-validation-rules.md) | POST |  |
| [List Validation Rules](actions/list-validation-rules.md) | GET |  |

### Workflow Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Data](actions/get-workflow-data.md) | GET |  |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow History](actions/get-workflow-history.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Delete Workflow](actions/delete-workflow.md) | DELETE |  |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Pause Workflow](actions/pause-workflow.md) | PUT |  |
| [Resume Workflow](actions/resume-workflow.md) | PUT |  |
| [Run Workflow](actions/run-workflow.md) | PUT |  |
| [Schedule Workflow](actions/schedule-workflow.md) | PUT |  |
| [Update Workflow Metadata](actions/update-workflow-metadata.md) | PUT |  |

