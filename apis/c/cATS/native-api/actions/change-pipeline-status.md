# Change Pipeline Status with CATS

Updates the status of a pipeline in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/pipelines/:id/status`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Change Pipeline Status](https://docs.catsone.com/api/v3/#pipelines-change-pipeline-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the pipeline that the status is being attached to. |
| `status_id` | body | `number` | yes | The ID of the status to attach. |
