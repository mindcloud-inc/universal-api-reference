# Scale: Native API Reference

A consolidated summary of Scale's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.genai.scale.com
- **API base URL:** `https://api.scale.com`

## Authentication

### API Key

Use a Scale API key as a Bearer token for all API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.genai.scale.com/get-started/authentication)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | `POST /v2/batch/cancel` | [docs](https://docs.genai.scale.com/v2/batch-cancel) |
| [Create Batch](actions/create-batch.md) | `POST /v2/batch` | [docs](https://docs.genai.scale.com/v2/batch-create) |
| [Create Chat Task](actions/create-chat-task.md) | `POST /v2/task/chat` | [docs](https://docs.genai.scale.com/v2/task-chat-create) |
| [Create Model Version Config](actions/create-model-version-config.md) | `POST /v2/model_version_configs` | [docs](https://docs.genai.scale.com/model-version-config-post) |
| [Finalize Batch](actions/finalize-batch.md) | `POST /v2/batch/finalize` | [docs](https://docs.genai.scale.com/v2/batch-finalize) |
| [Get Annotation](actions/get-annotation.md) | `GET /v2/annotation` | [docs](https://docs.genai.scale.com/v2/annotation) |
| [Get Autoeval Job Status](actions/get-autoeval-job-status.md) | `GET /v2/autoevals/{jobId}/status` | [docs](https://docs.genai.scale.com/status) |
| [Get Autoeval Model Version Config Statuses](actions/get-autoeval-model-version-config-statuses.md) | `GET /v2/autoevals/model_version_configs/{id}/statuses` | [docs](https://docs.genai.scale.com/model-statuses) |
| [Get Autoeval Results](actions/get-autoeval-results.md) | `GET /v2/autoevals/{jobId}/results` | [docs](https://docs.genai.scale.com/results) |
| [Get Batch](actions/get-batch.md) | `GET /v2/batch` | [docs](https://docs.genai.scale.com/v2/batch) |
| [Get Dataset Deliveries](actions/get-dataset-deliveries.md) | `GET /v2/datasets/deliveries` | [docs](https://docs.genai.scale.com/v2/datasets-deliveries) |
| [Get Dataset Delivery](actions/get-dataset-delivery.md) | `GET /v2/datasets/delivery` | [docs](https://docs.genai.scale.com/v2/datasets-delivery) |
| [Get Dataset Task](actions/get-dataset-task.md) | `GET /v2/datasets/task` | [docs](https://docs.genai.scale.com/v2/datasets-task) |
| [Get Delivery](actions/get-delivery.md) | `GET /v2/delivery` | [docs](https://docs.genai.scale.com/v2/delivery) |
| [Get Model Version Config](actions/get-model-version-config.md) | `GET /v2/model_version_configs/{id}` | [docs](https://docs.genai.scale.com/model-version-config-get) |
| [Get Multiple Projects](actions/get-multiple-projects.md) | `GET /v2/projects` | [docs](https://docs.genai.scale.com/v2/projects) |
| [Get Project](actions/get-project.md) | `GET /v2/project` | [docs](https://docs.genai.scale.com/v2/project) |
| [Get Schema](actions/get-schema.md) | `GET /v2/schema` | [docs](https://docs.genai.scale.com/v2/schema) |
| [Get Task](actions/get-task.md) | `GET /v2/task` | [docs](https://docs.genai.scale.com/v2/task) |
| [Get Task (Legacy)](actions/get-task-legacy.md) | `GET /v1/task/{task_id}` | [docs](https://docs.genai.scale.com/v1/task) |
| [Get Task Response Attachment URL](actions/get-task-response-attachment-url.md) | `GET /v2/datasets/task/{task_id}/response_url/{attachment_id}` | [docs](https://docs.genai.scale.com/v2/datasets-response_url) |
| [List Autoeval Statuses](actions/list-autoeval-statuses.md) | `GET /v2/autoevals/statuses` | [docs](https://docs.genai.scale.com/statuses) |
| [List Batches](actions/list-batches.md) | `GET /v2/batches` | [docs](https://docs.genai.scale.com/v2/batches) |
| [List Dataset Tasks](actions/list-dataset-tasks.md) | `GET /v2/datasets/tasks` | [docs](https://docs.genai.scale.com/v2/datasets-tasks) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://docs.genai.scale.com/v2/datasets) |
| [List Deliveries](actions/list-deliveries.md) | `GET /v2/deliveries` | [docs](https://docs.genai.scale.com/v2/deliveries) |
| [List Delivery Tasks](actions/list-delivery-tasks.md) | `GET /v2/delivery/tasks` | [docs](https://docs.genai.scale.com/v2/delivery-tasks) |
| [List Model Endpoints](actions/list-model-endpoints.md) | `GET /v2/model_endpoints` | [docs](https://docs.genai.scale.com/model-endpoints) |
| [List Model Version Configs](actions/list-model-version-configs.md) | `GET /v2/model_version_configs` | [docs](https://docs.genai.scale.com/model-version-configs) |
| [List Tasks](actions/list-tasks.md) | `GET /v2/tasks` | [docs](https://docs.genai.scale.com/v2/tasks) |
| [Pause Batch](actions/pause-batch.md) | `POST /v2/batch/pause` | [docs](https://docs.genai.scale.com/v2/batch-pause) |
| [Resume Batch](actions/resume-batch.md) | `POST /v2/batch/resume` | [docs](https://docs.genai.scale.com/v2/batch-resume) |
| [Retry Autoeval Job](actions/retry-autoeval-job.md) | `POST /v2/autoevals/retry` | [docs](https://docs.genai.scale.com/retry) |
| [Set Batch Metadata](actions/set-batch-metadata.md) | `POST /v2/batch/metadata` | [docs](https://docs.genai.scale.com/v2/batch-set-metadata) |
| [Set Task Metadata](actions/set-task-metadata.md) | `POST /v2/task/metadata` | [docs](https://docs.genai.scale.com/v2/task-set-metadata) |
| [Start Autoeval Job](actions/start-autoeval-job.md) | `POST /v2/autoevals` | [docs](https://docs.genai.scale.com/autoevals) |
| [Terminate Autoeval Job](actions/terminate-autoeval-job.md) | `POST /v2/autoevals/terminate` | [docs](https://docs.genai.scale.com/terminate) |
