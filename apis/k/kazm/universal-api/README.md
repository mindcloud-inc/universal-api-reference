# <img src="https://images.mindcloud.co/apps/icons/kazm-icon_1775070269677.png" alt="Kazm logo" width="28" height="28"> Kazm: Universal API

Kazm, now operating on the current Lightning Rod platform contract, lets teams generate datasets, manage files and file sets, run transform and training jobs, evaluate outputs, inspect organization balance, and call Lightning Rod's OpenAI-compatible endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kazm/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lightningrod.ai/
- **Vendor API docs:** https://docs.lightningrod.ai/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Balance](actions/get-organization-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-organization-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Chat Completions](actions/chat-completions.md) | POST | Creates a chat completion in Kazm. |

### Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Completion](actions/create-completion.md) | POST | Creates a completion in Kazm. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a dataset in Kazm. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Kazm. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Kazm. |

### Dataset Sample

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset Samples](actions/get-dataset-samples.md) | GET | Retrieves dataset samples from Kazm. |

### Dataset Sample Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Samples](actions/upload-samples.md) | POST | Uploads samples to a Kazm dataset. |

### Evaluation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Evaluation Job](actions/create-evaluation-job.md) | POST | Creates an evaluation job in Kazm. |
| [Get Evaluation Job](actions/get-evaluation-job.md) | GET | Retrieves an evaluation job from Kazm. |
| [List Evaluation Jobs](actions/list-evaluation-jobs.md) | GET | Retrieves evaluation jobs from Kazm. |

### File Retry

| Action | Method | Description |
| --- | --- | --- |
| [Retry Failed Files](actions/retry-failed-files.md) | POST | Retries failed files in a Kazm file set. |

### File Set

| Action | Method | Description |
| --- | --- | --- |
| [Create File Set](actions/create-file-set.md) | POST | Creates a file set in Kazm. |
| [Get File Set](actions/get-file-set.md) | GET | Retrieves a file set from Kazm. |
| [List File Sets](actions/list-file-sets.md) | GET | Retrieves file sets from Kazm. |

### File Set File

| Action | Method | Description |
| --- | --- | --- |
| [Add File To Set](actions/add-file-to-set.md) | POST | Adds a file to a Kazm file set. |
| [List Files In Set](actions/list-files-in-set.md) | GET | Retrieves files from a Kazm file set. |

### File Set Status

| Action | Method | Description |
| --- | --- | --- |
| [Get File Set Status](actions/get-file-set-status.md) | GET | Retrieves file set status from Kazm. |

### File Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create File Upload](actions/create-file-upload.md) | POST | Creates a file upload in Kazm. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves models from Kazm. |

### Organization Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Balance](actions/get-organization-balance.md) | GET | Retrieves the organization balance from Kazm. |

### Training Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Training Job](actions/create-training-job.md) | POST | Creates a training job in Kazm. |
| [Get Training Job](actions/get-training-job.md) | GET | Retrieves a training job from Kazm. |
| [List Training Jobs](actions/list-training-jobs.md) | GET | Retrieves training jobs from Kazm. |

### Training Job Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Training Cost](actions/estimate-training-cost.md) | GET | Retrieves a training cost estimate from Kazm. |

### Transform Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Transform Job](actions/cancel-transform-job.md) | DELETE | Cancels a transform job in Kazm. |
| [Create Transform Job](actions/create-transform-job.md) | POST | Creates a transform job in Kazm. |
| [Get Transform Job](actions/get-transform-job.md) | GET | Retrieves a transform job from Kazm. |
| [List Transform Jobs](actions/list-transform-jobs.md) | GET | Retrieves transform jobs from Kazm. |

### Transform Job Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Transform Job Cost](actions/estimate-transform-job-cost.md) | GET | Retrieves a transform job cost estimate from Kazm. |

### Transform Job Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Transform Job Metrics](actions/get-transform-job-metrics.md) | GET | Retrieves transform job metrics from Kazm. |

