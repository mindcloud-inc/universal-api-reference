# Viesus: Native API Reference

A consolidated summary of Viesus's API configuration and 43 documented operations, with links to official documentation.

- **Official docs:** https://docs.viesus.cloud
- **API base URL:** `https://api.viesus.cloud/graphql`

## Authentication

### Viesus API Key

Supply your Viesus Cloud API key. MindCloud sends it in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · optional · Your Viesus Cloud API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.viesus.cloud/reference/authentication)

## Endpoints (43 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze PDF](actions/analyze-pdf.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/pdf-analysis) |
| [Cancel Enhancement](actions/cancel-enhancement.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/enhancing) |
| [Complete Signed Upload](actions/complete-signed-upload.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/uploading/uploading-with-a-signed-upload-url) |
| [Create API Key](actions/create-api-key.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Create Enhanced Image](actions/create-enhanced-image.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/enhancing) |
| [Create Folder](actions/create-folder.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Create Signed Upload URL](actions/create-signed-upload-url.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/uploading/uploading-with-a-signed-upload-url) |
| [Create Upload From URL](actions/create-upload-from-url.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/uploading/uploading-from-a-url) |
| [Create Webhook](actions/create-webhook.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [Create Workflow](actions/create-workflow.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Delete API Key](actions/delete-api-key.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Delete Folder](actions/delete-folder.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Delete Uploads](actions/delete-uploads.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/remove-uploads) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [Delete Workflow](actions/delete-workflow.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get Account](actions/get-account.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get API Key Usage](actions/get-api-key-usage.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get API Version](actions/get-api-version.md) | `POST /` | [docs](https://docs.viesus.cloud/) |
| [Get Completed Enhanced Image](actions/get-completed-enhanced-image.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get Current User](actions/get-current-user.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get Enhanced Image](actions/get-enhanced-image.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/enhancing) |
| [Get Folder](actions/get-folder.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get Folder Breadcrumb](actions/get-folder-breadcrumb.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/remaining-credits) |
| [Get Upload](actions/get-upload.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/retrieving-enhancements) |
| [Get Webhook](actions/get-webhook.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [Get Workflow](actions/get-workflow.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List API Keys](actions/list-api-keys.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Folders](actions/list-folders.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Invoices](actions/list-invoices.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Payment Methods](actions/list-payment-methods.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Plans](actions/list-plans.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Tasks](actions/list-tasks.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Uploads](actions/list-uploads.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [List Webhooks](actions/list-webhooks.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [List Workflows](actions/list-workflows.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Refresh API Key](actions/refresh-api-key.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Update Folder](actions/update-folder.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Update Webhook](actions/update-webhook.md) | `POST /` | [docs](https://docs.viesus.cloud/reference/webhooks) |
| [Update Workflow Settings](actions/update-workflow-settings.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Update Workflow Triggers](actions/update-workflow-triggers.md) | `POST /` | [docs](https://docs.viesus.cloud) |
| [Upsert Enhanced Image Feedback](actions/upsert-enhanced-image-feedback.md) | `POST /` | [docs](https://docs.viesus.cloud) |
