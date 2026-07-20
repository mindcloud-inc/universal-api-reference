# Get backup creation status with Weaviate Vector Store

Retrieves backup creation status from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/backups/:backend/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get backup creation status](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | Specifies the backend storage system where the backup resides (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
| `id` | path | `string` | yes | The unique identifier of the backup. Must be URL-safe and compatible with filesystem paths (only lowercase, numbers, underscore, minus characters allowed). |
| `bucket` | query | `string` | no | Optional: Specifies the bucket, container, or volume name if required by the backend. |
| `path` | query | `string` | no | Optional: Specifies the path within the bucket/container/volume if the backup is not at the root. |
