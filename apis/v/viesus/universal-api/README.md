# <img src="https://images.mindcloud.co/apps/icons/viesus-favicon_1774978032743.png" alt="Viesus logo" width="28" height="28"> Viesus: Universal API

Viesus Cloud GraphQL API for image and PDF enhancement workflows, uploads, folders, webhooks, workflows, and credit usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/viesus/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 43
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.viesus.com
- **Vendor API docs:** https://docs.viesus.cloud

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (43)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves the current account in Viesus. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Viesus. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an API key from Viesus. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from your Viesus account. |
| [Refresh API Key](actions/refresh-api-key.md) | PUT | Refreshes an API key in Viesus. |

### Api Key Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Usage](actions/get-api-key-usage.md) | GET | Retrieves API key usage from Viesus. |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET | Retrieves the current Viesus API version. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET | Retrieves the remaining credits in Viesus. |

### Enhanced Image

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Enhancement](actions/cancel-enhancement.md) | PUT | Cancels an image enhancement in Viesus. |
| [Create Enhanced Image](actions/create-enhanced-image.md) | POST | Creates an enhanced image in Viesus. |
| [Get Completed Enhanced Image](actions/get-completed-enhanced-image.md) | GET | Retrieves a completed enhanced image from Viesus. |
| [Get Enhanced Image](actions/get-enhanced-image.md) | GET | Retrieves an enhanced image from Viesus. |
| [Upsert Enhanced Image Feedback](actions/upsert-enhanced-image-feedback.md) | PUT | Creates or updates enhanced image feedback in Viesus. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Analyze PDF](actions/analyze-pdf.md) | PUT | Analyzes a PDF upload in Viesus. |
| [Complete Signed Upload](actions/complete-signed-upload.md) | PUT | Completes a signed upload in Viesus. |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | POST | Creates a signed upload URL in Viesus. |
| [Create Upload From URL](actions/create-upload-from-url.md) | POST | Creates an upload in Viesus from a URL. |
| [Delete Uploads](actions/delete-uploads.md) | DELETE | Deletes uploaded files from your Viesus account. |
| [Get Upload](actions/get-upload.md) | GET | Retrieves an upload record from Viesus. |
| [List Uploads](actions/list-uploads.md) | GET | Retrieves uploads from your Viesus account. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Viesus. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Viesus. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder record from Viesus. |
| [Get Folder Breadcrumb](actions/get-folder-breadcrumb.md) | GET | Retrieves a folder breadcrumb from Viesus. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your Viesus account. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Viesus. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Viesus account. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from your Viesus account. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves available subscription plans from Viesus. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Viesus account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Viesus. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Viesus. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Viesus. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook endpoint from Viesus. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook endpoints from your Viesus account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Viesus. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Retrieves webhook delivery logs from Viesus. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Viesus. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from Viesus. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow record from Viesus. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from your Viesus account. |
| [Update Workflow Settings](actions/update-workflow-settings.md) | PUT | Updates workflow settings in your Viesus account. |
| [Update Workflow Triggers](actions/update-workflow-triggers.md) | PUT | Updates workflow triggers in your Viesus account. |

