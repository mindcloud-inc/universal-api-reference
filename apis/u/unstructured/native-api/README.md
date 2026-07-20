# Unstructured: Native API Reference

A consolidated summary of Unstructured's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://docs.unstructured.io/api-reference/quickstart
- **API base URL:** `https://platform.unstructuredapp.io/api/v1`

## Authentication

### API Key

Send the Unstructured API key in the unstructured-api-key request header.

### Credentials

- **API Key:** `apiKey` · required · Your Unstructured API key. MindCloud sends it as the unstructured-api-key header on every request.

Send these headers with each API request:

```http
unstructured-api-key: <apiKey>
```

[Official authentication documentation](https://docs.unstructured.io/api-reference/troubleshooting/api-key-url)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | `POST /jobs/:job_id/cancel` | [docs](https://docs.unstructured.io/api-reference/jobs/cancel-job) |
| [Create Destination Connection Check](actions/create-destination-connection-check.md) | `POST /destinations/:destination_id/connection-check` | [docs](https://docs.unstructured.io/api-reference/destinations/create-destination-connection-check) |
| [Create Destination Connector](actions/create-destination-connector.md) | `POST /destinations/` | [docs](https://docs.unstructured.io/api-reference/destinations/create-destination-connector) |
| [Create On-Demand Job](actions/create-on-demand-job.md) | `POST /jobs/` | [docs](https://docs.unstructured.io/api-reference/quickstart) |
| [Create Source Connection Check](actions/create-source-connection-check.md) | `POST /sources/:source_id/connection-check` | [docs](https://docs.unstructured.io/api-reference/sources/create-source-connection-check) |
| [Create Source Connector](actions/create-source-connector.md) | `POST /sources/` | [docs](https://docs.unstructured.io/api-reference/sources/create-source-connector) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows/` | [docs](https://docs.unstructured.io/api-reference/workflows/create-workflow) |
| [Create Workflow Channel](actions/create-workflow-channel.md) | `POST /workflows/:workflow_id/notifications/channels` | [docs](https://docs.unstructured.io/api-reference/workflows/create-workflow-channel) |
| [Create Workflow Notification Channel](actions/create-workflow-notification-channel.md) | `POST /workflows/:workflow_id/notifications/channels` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Create Workspace Notification Channel](actions/create-workspace-notification-channel.md) | `POST /notifications/channels` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Delete Destination Connector](actions/delete-destination-connector.md) | `DELETE /destinations/:destination_id` | [docs](https://docs.unstructured.io/api-reference/destinations/delete-destination-connector) |
| [Delete Source Connector](actions/delete-source-connector.md) | `DELETE /sources/:source_id` | [docs](https://docs.unstructured.io/api-reference/sources/delete-source-connector) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflows/:workflow_id` | [docs](https://docs.unstructured.io/api-reference/workflows/delete-workflow) |
| [Delete Workflow Channel](actions/delete-workflow-channel.md) | `DELETE /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/workflows/delete-workflow-channel) |
| [Delete Workflow Notification Channel](actions/delete-workflow-notification-channel.md) | `DELETE /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Delete Workspace Notification Channel](actions/delete-workspace-notification-channel.md) | `DELETE /notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Download Job Output](actions/download-job-output.md) | `GET /jobs/:job_id/download` | [docs](https://docs.unstructured.io/api-reference/jobs/download-job-output) |
| [Get Destination Connection Check](actions/get-destination-connection-check.md) | `GET /destinations/:destination_id/connection-check` | [docs](https://docs.unstructured.io/api-reference/destinations/get-destination-connection-check) |
| [Get Destination Connector](actions/get-destination-connector.md) | `GET /destinations/:destination_id` | [docs](https://docs.unstructured.io/api-reference/destinations/get-destination-connector) |
| [Get Failed Files](actions/get-failed-files.md) | `GET /jobs/:job_id/failed-files` | [docs](https://docs.unstructured.io/api-reference/jobs/get-failed-files) |
| [Get Job](actions/get-job.md) | `GET /jobs/:job_id` | [docs](https://docs.unstructured.io/api-reference/jobs/get-job) |
| [Get Job Details](actions/get-job-details.md) | `GET /jobs/:job_id/details` | [docs](https://docs.unstructured.io/api-reference/jobs/get-job-details) |
| [Get Notification](actions/get-notification.md) | `GET /notifications/:notification_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Get Source Connection Check](actions/get-source-connection-check.md) | `GET /sources/:source_id/connection-check` | [docs](https://docs.unstructured.io/api-reference/sources/get-source-connection-check) |
| [Get Source Connector](actions/get-source-connector.md) | `GET /sources/:source_id` | [docs](https://docs.unstructured.io/api-reference/sources/get-source-connector) |
| [Get Template](actions/get-template.md) | `GET /templates/:template_id` | [docs](https://docs.unstructured.io/api-reference/templates/get-template) |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | `GET /notifications/unread-count` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflow_id` | [docs](https://docs.unstructured.io/api-reference/workflows/get-workflow) |
| [Get Workflow Channel](actions/get-workflow-channel.md) | `GET /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/workflows/get-workflow-channel) |
| [Get Workflow Notification Channel](actions/get-workflow-notification-channel.md) | `GET /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Get Workspace Notification Channel](actions/get-workspace-notification-channel.md) | `GET /notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [List Destination Connectors](actions/list-destination-connectors.md) | `GET /destinations/` | [docs](https://docs.unstructured.io/api-reference/destinations/list-destination-connectors) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs/` | [docs](https://docs.unstructured.io/api-reference/jobs/list-jobs) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [List Source Connectors](actions/list-source-connectors.md) | `GET /sources/` | [docs](https://docs.unstructured.io/api-reference/sources/list-source-connectors) |
| [List Templates](actions/list-templates.md) | `GET /templates/` | [docs](https://docs.unstructured.io/api-reference/templates/list-templates) |
| [List Workflow Channels](actions/list-workflow-channels.md) | `GET /workflows/:workflow_id/notifications/channels` | [docs](https://docs.unstructured.io/api-reference/workflows/list-workflow-channels) |
| [List Workflow Notification Channels](actions/list-workflow-notification-channels.md) | `GET /workflows/:workflow_id/notifications/channels` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows/` | [docs](https://docs.unstructured.io/api-reference/workflows/list-workflows) |
| [List Workspace Notification Channels](actions/list-workspace-notification-channels.md) | `GET /notifications/channels` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Mark Notifications As Read](actions/mark-notifications-as-read.md) | `POST /notifications/mark-read` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Run Workflow](actions/run-workflow.md) | `POST /workflows/:workflow_id/run` | [docs](https://docs.unstructured.io/api-reference/workflows/run-workflow) |
| [Update Destination Connector](actions/update-destination-connector.md) | `PUT /destinations/:destination_id` | [docs](https://docs.unstructured.io/api-reference/destinations/update-destination-connector) |
| [Update Source Connector](actions/update-source-connector.md) | `PUT /sources/:source_id` | [docs](https://docs.unstructured.io/api-reference/sources/update-source-connector) |
| [Update Workflow](actions/update-workflow.md) | `PUT /workflows/:workflow_id` | [docs](https://docs.unstructured.io/api-reference/workflows/update-workflow) |
| [Update Workflow Channel](actions/update-workflow-channel.md) | `PATCH /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/workflows/update-workflow-channel) |
| [Update Workflow Notification Channel](actions/update-workflow-notification-channel.md) | `PATCH /workflows/:workflow_id/notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Update Workspace Notification Channel](actions/update-workspace-notification-channel.md) | `PATCH /notifications/channels/:channel_id` | [docs](https://docs.unstructured.io/api-reference/webhooks) |
| [Verify Workflow Channel](actions/verify-workflow-channel.md) | `POST /workflows/:workflow_id/notifications/channels/:channel_id/verify` | [docs](https://docs.unstructured.io/api-reference/workflows/verify-workflow-channel) |
