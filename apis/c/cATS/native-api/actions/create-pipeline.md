# Create Pipeline with CATS

Creates a new pipeline in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/pipelines`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Pipeline](https://docs.catsone.com/api/v3/#pipelines-create-a-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | body | `number` | yes | The candidate ID for the pipeline. |
| `job_id` | body | `number` | yes | The job ID for the pipeline. |
| `rating` | body | `number` | no | The candidate rating for the job. |
