# Kazm: Native API Reference

A consolidated summary of Kazm's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.lightningrod.ai/rest-api
- **API base URL:** `https://api.lightningrod.ai/api/public/v1`

## Authentication

### API Key

Use your Lightning Rod API key. The runtime sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.lightningrod.ai/rest-api)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File To Set](actions/add-file-to-set.md) | `POST /filesets/:fileSetId/files` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [Cancel Transform Job](actions/cancel-transform-job.md) | `DELETE /transform-jobs/:jobId` | [docs](https://docs.lightningrod.ai/rest-api/datasets) |
| [Chat Completions](actions/chat-completions.md) | `POST /openai/chat/completions` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [Create Completion](actions/create-completion.md) | `POST /openai/completions` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [Create Dataset](actions/create-dataset.md) | `POST /datasets` | [docs](https://docs.lightningrod.ai/rest-api/datasets) |
| [Create Evaluation Job](actions/create-evaluation-job.md) | `POST /evaluations` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [Create File Set](actions/create-file-set.md) | `POST /filesets` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [Create File Upload](actions/create-file-upload.md) | `POST /files` | [docs](https://docs.lightningrod.ai/rest-api/training-jobs) |
| [Create Training Job](actions/create-training-job.md) | `POST /training-jobs` | [docs](https://docs.lightningrod.ai/rest-api/training-jobs) |
| [Create Transform Job](actions/create-transform-job.md) | `POST /transform-jobs` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [Estimate Training Cost](actions/estimate-training-cost.md) | `POST /training-jobs/cost-estimation` | [docs](https://docs.lightningrod.ai/rest-api/evaluations) |
| [Estimate Transform Job Cost](actions/estimate-transform-job-cost.md) | `POST /transform-jobs/cost-estimation` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [Get Dataset](actions/get-dataset.md) | `GET /datasets/:datasetId` | [docs](https://docs.lightningrod.ai/rest-api/files) |
| [Get Dataset Samples](actions/get-dataset-samples.md) | `GET /datasets/:datasetId/samples` | [docs](https://docs.lightningrod.ai/rest-api/training-jobs) |
| [Get Evaluation Job](actions/get-evaluation-job.md) | `GET /evaluations/:evalId` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [Get File Set](actions/get-file-set.md) | `GET /filesets/:fileSetId` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [Get File Set Status](actions/get-file-set-status.md) | `GET /filesets/:fileSetId/status` | [docs](https://docs.lightningrod.ai/rest-api) |
| [Get Organization Balance](actions/get-organization-balance.md) | `GET /organizations/balance` | [docs](https://docs.lightningrod.ai/rest-api/organizations) |
| [Get Training Job](actions/get-training-job.md) | `GET /training-jobs/:jobId` | [docs](https://docs.lightningrod.ai/rest-api/evaluations) |
| [Get Transform Job](actions/get-transform-job.md) | `GET /transform-jobs/:jobId` | [docs](https://docs.lightningrod.ai/rest-api/datasets) |
| [Get Transform Job Metrics](actions/get-transform-job-metrics.md) | `GET /transform-jobs/:jobId/metrics` | [docs](https://docs.lightningrod.ai/rest-api/datasets) |
| [List Datasets](actions/list-datasets.md) | `GET /datasets` | [docs](https://docs.lightningrod.ai/rest-api/datasets) |
| [List Evaluation Jobs](actions/list-evaluation-jobs.md) | `GET /evaluations` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [List File Sets](actions/list-file-sets.md) | `GET /filesets` | [docs](https://docs.lightningrod.ai/rest-api/filesets) |
| [List Files In Set](actions/list-files-in-set.md) | `GET /filesets/:fileSetId/files` | [docs](https://docs.lightningrod.ai/rest-api) |
| [List Models](actions/list-models.md) | `GET /openai/models` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [List Training Jobs](actions/list-training-jobs.md) | `GET /training-jobs` | [docs](https://docs.lightningrod.ai/rest-api/evaluations) |
| [List Transform Jobs](actions/list-transform-jobs.md) | `GET /transform-jobs` | [docs](https://docs.lightningrod.ai/rest-api/transform-jobs) |
| [Retry Failed Files](actions/retry-failed-files.md) | `POST /filesets/:fileSetId/retry-failed` | [docs](https://docs.lightningrod.ai/rest-api) |
| [Upload Samples](actions/upload-samples.md) | `POST /datasets/:datasetId/samples` | [docs](https://docs.lightningrod.ai/rest-api/training-jobs) |
