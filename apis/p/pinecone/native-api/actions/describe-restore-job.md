# Describe Restore Job with Pinecone

Retrieves details for a restore job from Pinecone.

## Endpoint

- **Method:** `GET`
- **Path:** `/restore-jobs/:job_id`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Describe Restore Job](https://docs.pinecone.io/reference/api/2025-10/control-plane/describe_restore_job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The ID of the restore job to describe. |
