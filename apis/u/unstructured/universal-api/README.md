# <img src="https://images.mindcloud.co/apps/icons/unstructured_1776196625158.png" alt="Unstructured logo" width="28" height="28"> Unstructured: Universal API

Unstructured document ingestion and workflow API for templates, source connectors, destination connectors, workflows, and jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unstructured/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unstructured.io
- **Vendor API docs:** https://docs.unstructured.io/api-reference/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Channel](actions/create-workflow-channel.md) | POST | Creates a workflow notification channel in Unstructured. |
| [Create Workspace Notification Channel](actions/create-workspace-notification-channel.md) | POST | Creates a workspace notification channel in Unstructured. |
| [Delete Workflow Channel](actions/delete-workflow-channel.md) | DELETE | Deletes a workflow notification channel from Unstructured. |
| [Delete Workspace Notification Channel](actions/delete-workspace-notification-channel.md) | DELETE | Deletes a workspace notification channel from Unstructured. |
| [Get Workflow Channel](actions/get-workflow-channel.md) | GET | Retrieves a workflow notification channel from Unstructured. |
| [Get Workspace Notification Channel](actions/get-workspace-notification-channel.md) | GET | Retrieves a workspace notification channel from Unstructured. |
| [List Workflow Channels](actions/list-workflow-channels.md) | GET | Retrieves workflow notification channels from Unstructured. |
| [List Workspace Notification Channels](actions/list-workspace-notification-channels.md) | GET | Retrieves workspace notification channels from Unstructured. |
| [Update Workflow Channel](actions/update-workflow-channel.md) | PUT | Updates a workflow notification channel in Unstructured. |
| [Update Workspace Notification Channel](actions/update-workspace-notification-channel.md) | PUT | Updates a workspace notification channel in Unstructured. |
| [Verify Workflow Channel](actions/verify-workflow-channel.md) | PUT | Verifies a workflow notification channel in Unstructured. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Destination Connection Check](actions/create-destination-connection-check.md) | POST | Creates a destination connection check in Unstructured. |
| [Create Destination Connector](actions/create-destination-connector.md) | POST | Creates a destination connector in Unstructured. |
| [Create Source Connection Check](actions/create-source-connection-check.md) | POST | Creates a source connection check in Unstructured. |
| [Create Source Connector](actions/create-source-connector.md) | POST | Creates a source connector in Unstructured. |
| [Delete Destination Connector](actions/delete-destination-connector.md) | DELETE | Deletes a destination connector from Unstructured. |
| [Delete Source Connector](actions/delete-source-connector.md) | DELETE | Deletes a source connector from Unstructured. |
| [Get Destination Connection Check](actions/get-destination-connection-check.md) | GET | Retrieves a destination connection check from Unstructured. |
| [Get Destination Connector](actions/get-destination-connector.md) | GET | Retrieves a destination connector from Unstructured. |
| [Get Source Connection Check](actions/get-source-connection-check.md) | GET | Retrieves a source connection check from Unstructured. |
| [Get Source Connector](actions/get-source-connector.md) | GET | Retrieves a source connector from Unstructured. |
| [List Destination Connectors](actions/list-destination-connectors.md) | GET | Retrieves a list of destination connectors from Unstructured. |
| [List Source Connectors](actions/list-source-connectors.md) | GET | Retrieves a list of source connectors from Unstructured. |
| [Update Destination Connector](actions/update-destination-connector.md) | PUT | Updates a destination connector in Unstructured. |
| [Update Source Connector](actions/update-source-connector.md) | PUT | Updates a source connector in Unstructured. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET | Retrieves a notification from Unstructured. |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | GET | Retrieves the unread notification count from Unstructured. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Unstructured. |
| [Mark Notifications As Read](actions/mark-notifications-as-read.md) | PUT | Marks notifications as read in Unstructured. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Unstructured. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from Unstructured. |

### Workflow Notification Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Notification Channel](actions/create-workflow-notification-channel.md) | POST | Creates a workflow notification channel in Unstructured. |
| [Delete Workflow Notification Channel](actions/delete-workflow-notification-channel.md) | DELETE | Deletes a workflow notification channel from Unstructured. |
| [Get Workflow Notification Channel](actions/get-workflow-notification-channel.md) | GET | Retrieves a workflow notification channel from Unstructured. |
| [List Workflow Notification Channels](actions/list-workflow-notification-channels.md) | GET | Retrieves workflow notification channels from Unstructured. |
| [Update Workflow Notification Channel](actions/update-workflow-notification-channel.md) | PUT | Updates a workflow notification channel in Unstructured. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | PUT | Cancels a job in Unstructured. |
| [Create On-Demand Job](actions/create-on-demand-job.md) | POST | Creates an on-demand job in Unstructured. |
| [Download Job Output](actions/download-job-output.md) | GET | Downloads job output from Unstructured. |
| [Get Failed Files](actions/get-failed-files.md) | GET | Retrieves failed files for a job from Unstructured. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Unstructured. |
| [Get Job Details](actions/get-job-details.md) | GET | Retrieves job details from Unstructured. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves a list of jobs from Unstructured. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a workflow in Unstructured. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes a workflow from Unstructured. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Unstructured. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves a list of workflows from Unstructured. |
| [Run Workflow](actions/run-workflow.md) | PUT | Runs a workflow in Unstructured. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates a workflow in Unstructured. |

