# <img src="https://images.mindcloud.co/apps/icons/scale-icon_1775829831160.png" alt="Scale logo" width="28" height="28"> Scale: Universal API

Scale provides APIs for GenAI project management, task operations, dataset deliveries, model version configuration, and auto-evaluation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scale/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scale.com
- **Vendor API docs:** https://docs.genai.scale.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Multiple Projects](actions/get-multiple-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | GET |  |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset Deliveries](actions/get-dataset-deliveries.md) | GET |  |
| [Get Dataset Delivery](actions/get-dataset-delivery.md) | GET |  |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Model Endpoints](actions/list-model-endpoints.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Response Attachment URL](actions/get-task-response-attachment-url.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Retry Autoeval Job](actions/retry-autoeval-job.md) | PUT |  |
| [Start Autoeval Job](actions/start-autoeval-job.md) | POST |  |
| [Terminate Autoeval Job](actions/terminate-autoeval-job.md) | PUT |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Model Version Config](actions/create-model-version-config.md) | POST |  |
| [Get Model Version Config](actions/get-model-version-config.md) | GET |  |
| [List Model Version Configs](actions/list-model-version-configs.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Multiple Projects](actions/get-multiple-projects.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Autoeval Results](actions/get-autoeval-results.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Autoeval Job Status](actions/get-autoeval-job-status.md) | GET |  |
| [Get Autoeval Model Version Config Statuses](actions/get-autoeval-model-version-config-statuses.md) | GET |  |
| [List Autoeval Statuses](actions/list-autoeval-statuses.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Task](actions/create-chat-task.md) | POST |  |
| [Get Dataset Task](actions/get-dataset-task.md) | GET |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Get Task (Legacy)](actions/get-task-legacy.md) | GET |  |
| [List Dataset Tasks](actions/list-dataset-tasks.md) | GET |  |
| [List Delivery Tasks](actions/list-delivery-tasks.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Set Task Metadata](actions/set-task-metadata.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT |  |
| [Create Batch](actions/create-batch.md) | POST |  |
| [Finalize Batch](actions/finalize-batch.md) | PUT |  |
| [Get Annotation](actions/get-annotation.md) | GET |  |
| [Get Batch](actions/get-batch.md) | GET |  |
| [Get Delivery](actions/get-delivery.md) | GET |  |
| [Get Schema](actions/get-schema.md) | GET |  |
| [List Batches](actions/list-batches.md) | GET |  |
| [List Deliveries](actions/list-deliveries.md) | GET |  |
| [Pause Batch](actions/pause-batch.md) | PUT |  |
| [Resume Batch](actions/resume-batch.md) | PUT |  |
| [Set Batch Metadata](actions/set-batch-metadata.md) | PUT |  |

