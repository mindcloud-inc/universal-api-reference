# Change Job Status with CATS

Updates the status of a job in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:id/status`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Change Job Status](https://docs.catsone.com/api/v3/#jobs-change-job-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the job that the status is being attached to. |
| `status_id` | body | `number` | yes | The ID of the status to attach. |
