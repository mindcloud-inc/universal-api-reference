# Cancel a backup restoration with Weaviate Vector Store

Cancels a backup restoration in Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/backups/:backend/:id/restore`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Cancel a backup restoration](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | Specifies the backend storage system where the backup resides (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
| `id` | path | `string` | yes | The unique identifier of the backup restoration to cancel. Must be URL-safe and compatible with filesystem paths (only lowercase, numbers, underscore, minus characters allowed). |
| `bucket` | query | `string` | no | Optional: Specifies the bucket, container, or volume name if required by the backend. |
| `path` | query | `string` | no | Optional: Specifies the path within the bucket/container/volume if the backup is not at the root. |
