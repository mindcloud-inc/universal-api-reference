# Delete Job with Eranol

Deletes an existing processing job from Eranol.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ffmpeg/jobs/:job_id`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Delete Job](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Job ID returned by an Eranol create action. |
