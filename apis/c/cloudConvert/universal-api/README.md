# <img src="https://images.mindcloud.co/apps/icons/logo_1775242370858.png" alt="CloudConvert logo" width="28" height="28"> CloudConvert: Universal API

Convert files, documents, images, video, audio, and PDFs through CloudConvert jobs and tasks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudConvert/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudconvert.com
- **Vendor API docs:** https://cloudconvert.com/docs/getting-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Format

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Formats](actions/list-supported-formats.md) | GET | Retrieves supported conversion formats from CloudConvert. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a job in your CloudConvert account. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes a job from your CloudConvert account. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from your CloudConvert account. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from your CloudConvert account. |
| [Wait for Job](actions/wait-for-job.md) | GET | Waits for a CloudConvert job to finish. |

### Operation

| Action | Method | Description |
| --- | --- | --- |
| [List Possible Operations](actions/list-possible-operations.md) | GET | Retrieves available file operations from CloudConvert. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | PUT | Cancels a task in your CloudConvert account. |
| [Create Archive Task](actions/create-archive-task.md) | POST | Creates an archive task in CloudConvert. |
| [Create Convert Task](actions/create-convert-task.md) | POST | Creates a convert task in CloudConvert. |
| [Create Export URL Task](actions/create-export-url-task.md) | POST | Creates an export-by-URL task in CloudConvert. |
| [Create Import URL Task](actions/create-import-url-task.md) | POST | Creates an import-by-URL task in CloudConvert. |
| [Create Merge Task](actions/create-merge-task.md) | POST | Creates a merge task in CloudConvert. |
| [Create Metadata Task](actions/create-metadata-task.md) | POST | Creates a metadata task in CloudConvert. |
| [Create Upload Task](actions/create-upload-task.md) | POST | Creates an upload task in CloudConvert. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from your CloudConvert account. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from your CloudConvert account. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your CloudConvert account. |
| [Retry Task](actions/retry-task.md) | POST | Retries a task in your CloudConvert account. |
| [Wait for Task](actions/wait-for-task.md) | GET | Waits for a CloudConvert task to finish. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from CloudConvert. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in your CloudConvert account. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from your CloudConvert account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your CloudConvert account. |

