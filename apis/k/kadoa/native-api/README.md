# Kadoa: Native API Reference

A consolidated summary of Kadoa's API configuration and 44 documented operations, with links to official documentation.

- **Official docs:** https://docs.kadoa.com/api-reference/introduction
- **API base URL:** `https://api.kadoa.com`

## Authentication

### API Key

Use Kadoa API key via x-api-key header

### Credentials

- **API Key:** `apiKey` · required · Kadoa API key from your account settings

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.kadoa.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (44 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Approve Rules](actions/bulk-approve-rules.md) | `POST /v4/data-validation/rules/actions/bulk-approve` | [docs](https://docs.kadoa.com/docs/ui/data-validation) |
| [Bulk Delete Rules](actions/bulk-delete-rules.md) | `POST /v4/data-validation/rules/actions/bulk-delete` | [docs](https://docs.kadoa.com/docs/ui/data-validation) |
| [Create Notification Channel](actions/create-notification-channel.md) | `POST /v5/notifications/channels` | [docs](https://docs.kadoa.com/api-reference/notifications/create-notification-channel) |
| [Create Notification Settings](actions/create-notification-settings.md) | `POST /v5/notifications/settings` | [docs](https://docs.kadoa.com/api-reference/notifications/create-notification-settings) |
| [Create Schema](actions/create-schema.md) | `POST /v4/schemas/` | [docs](https://docs.kadoa.com/api-reference/schemas/create-schema) |
| [Create Workflow](actions/create-workflow.md) | `POST /v4/workflows/` | [docs](https://docs.kadoa.com/api-reference/workflows/create-a-new-workflow) |
| [Delete Notification Channel](actions/delete-notification-channel.md) | `DELETE /v5/notifications/channels/:channelId` | [docs](https://docs.kadoa.com/api-reference/notifications/delete-notification-channel) |
| [Delete Notification Settings](actions/delete-notification-settings.md) | `DELETE /v5/notifications/settings/:settingsId` | [docs](https://docs.kadoa.com/api-reference/notifications/delete-notification-settings) |
| [Delete Schema](actions/delete-schema.md) | `DELETE /v4/schemas/:schemaId` | [docs](https://docs.kadoa.com/api-reference/schemas/delete-schema) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /v4/workflows/:workflowId` | [docs](https://docs.kadoa.com/api-reference/workflows/delete-a-workflow) |
| [Extract Data](actions/extract-data.md) | `POST /v4/adhoc/:schemaId` | [docs](https://docs.kadoa.com/api-reference/introduction) |
| [Generate Validation Rules](actions/generate-validation-rules.md) | `POST /v4/data-validation/rules/actions/generate` | [docs](https://docs.kadoa.com/api-reference/data-validation/generate-rules) |
| [Get Change](actions/get-change.md) | `GET /v4/changes/:changeId` | [docs](https://docs.kadoa.com/api-reference/monitoring/get-change-by-id) |
| [Get Crawl Page Content](actions/get-crawl-page-content.md) | `GET /v4/crawl/:sessionId/pages/:pageId` | [docs](https://docs.kadoa.com/api-reference/crawling/get-crawled-page-meta) |
| [Get Crawl Pages](actions/get-crawl-pages.md) | `GET /v4/crawl/:sessionId/pages` | [docs](https://docs.kadoa.com/api-reference/crawling/get-crawled-pages) |
| [Get Crawl Status](actions/get-crawl-status.md) | `GET /v4/crawl/:sessionId/status` | [docs](https://docs.kadoa.com/api-reference/crawling/crawling-session-status) |
| [Get Event Type](actions/get-event-type.md) | `GET /v5/notifications/event-types/:eventType` | [docs](https://docs.kadoa.com/api-reference/notifications/get-event-type) |
| [Get Notification Channel](actions/get-notification-channel.md) | `GET /v5/notifications/channels/:channelId` | [docs](https://docs.kadoa.com/api-reference/notifications/get-notification-channel) |
| [Get Notification Settings](actions/get-notification-settings.md) | `GET /v5/notifications/settings/:settingsId` | [docs](https://docs.kadoa.com/api-reference/notifications/get-notification-setting) |
| [Get Schema](actions/get-schema.md) | `GET /v4/schemas/:schemaId` | [docs](https://docs.kadoa.com/api-reference/schemas/get-schema-by-id) |
| [Get Validation Config](actions/get-validation-config.md) | `GET /v4/data-validation/workflows/:workflowId/validation/config` | [docs](https://docs.kadoa.com/api-reference/data-validation/validation-config) |
| [Get Validation Results](actions/get-validation-results.md) | `GET /v4/data-validation/workflows/:workflowId/jobs/:jobId/validations/latest` | [docs](https://docs.kadoa.com/api-reference/data-validation/latest-validation) |
| [Get Workflow](actions/get-workflow.md) | `GET /v4/workflows/:workflowId` | [docs](https://docs.kadoa.com/api-reference/workflows/get-workflow-by-id) |
| [Get Workflow Data](actions/get-workflow-data.md) | `GET /v4/workflows/:workflowId/data` | [docs](https://docs.kadoa.com/api-reference/workflows/get-workflow-data-by-id) |
| [Get Workflow History](actions/get-workflow-history.md) | `GET /v4/workflows/:workflowId/history` | [docs](https://docs.kadoa.com/api-reference/workflows/get-the-workflow-history) |
| [List Changes](actions/list-changes.md) | `GET /v4/changes` | [docs](https://docs.kadoa.com/api-reference/monitoring/get-all-changes) |
| [List Event Types](actions/list-event-types.md) | `GET /v5/notifications/event-types` | [docs](https://docs.kadoa.com/api-reference/notifications/get-event-types) |
| [List Locations](actions/list-locations.md) | `GET /v4/locations` | [docs](https://docs.kadoa.com/api-reference/locations/get-all-locations) |
| [List Notification Channels](actions/list-notification-channels.md) | `GET /v5/notifications/channels` | [docs](https://docs.kadoa.com/api-reference/notifications/get-notification-channels) |
| [List Notification Settings](actions/list-notification-settings.md) | `GET /v5/notifications/settings` | [docs](https://docs.kadoa.com/api-reference/notifications/get-notification-settings) |
| [List Schemas](actions/list-schemas.md) | `GET /v4/schemas/` | [docs](https://docs.kadoa.com/api-reference/schemas/get-all-schemas) |
| [List Validation Rules](actions/list-validation-rules.md) | `GET /v4/data-validation/rules` | [docs](https://docs.kadoa.com/api-reference/data-validation/list-rules) |
| [List Workflows](actions/list-workflows.md) | `GET /v4/workflows` | [docs](https://docs.kadoa.com/api-reference/workflows/get-all-workflows) |
| [Pause Workflow](actions/pause-workflow.md) | `PUT /v4/workflows/:workflowId/pause` | [docs](https://docs.kadoa.com/api-reference/workflows/pause-a-workflow) |
| [Resume Workflow](actions/resume-workflow.md) | `PUT /v4/workflows/:workflowId/resume` | [docs](https://docs.kadoa.com/api-reference/workflows/resume-a-workflow) |
| [Run Workflow](actions/run-workflow.md) | `PUT /v4/workflows/:workflowId/run` | [docs](https://docs.kadoa.com/api-reference/workflows/run-a-workflow) |
| [Schedule Workflow](actions/schedule-workflow.md) | `PUT /v4/workflows/:workflowId/schedule` | [docs](https://docs.kadoa.com/api-reference/workflows/schedule-a-workflow) |
| [Start Crawl](actions/start-crawl.md) | `POST /v4/crawl/` | [docs](https://docs.kadoa.com/api-reference/crawling/start-crawling-session) |
| [Test Notification](actions/test-notification.md) | `POST /v5/notifications/test` | [docs](https://docs.kadoa.com/api-reference/notifications/test-notifications) |
| [Toggle Validation](actions/toggle-validation.md) | `PUT /v4/data-validation/workflows/:workflowId/validation/toggle` | [docs](https://docs.kadoa.com/api-reference/data-validation/toggle-validation) |
| [Update Notification Channel](actions/update-notification-channel.md) | `PUT /v5/notifications/channels/:channelId` | [docs](https://docs.kadoa.com/api-reference/notifications/update-notification-channel) |
| [Update Notification Settings](actions/update-notification-settings.md) | `PUT /v5/notifications/settings/:settingsId` | [docs](https://docs.kadoa.com/api-reference/notifications/update-notification-settings) |
| [Update Schema](actions/update-schema.md) | `PUT /v4/schemas/:schemaId` | [docs](https://docs.kadoa.com/api-reference/schemas/update-schema) |
| [Update Workflow Metadata](actions/update-workflow-metadata.md) | `PUT /v4/workflows/:workflowId/metadata` | [docs](https://docs.kadoa.com/api-reference/workflows/update-workflow-metadata) |
