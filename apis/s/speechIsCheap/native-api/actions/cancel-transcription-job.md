# Cancel Transcription Job with Speech is Cheap

Deletes a pending transcription job from Speech is Cheap.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs/:job_id`
- **Base URL:** `https://api.speechischeap.com/v2`
- **Official documentation:** [Cancel Transcription Job](https://docs.speechischeap.com/jobs-v2/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Speech is Cheap transcription job ID to cancel. |
