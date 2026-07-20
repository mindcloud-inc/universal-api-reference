# Restore from a backup with Weaviate Vector Store

Restores from a backup in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/backups/:backend/:id/restore`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Restore from a backup](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | Specifies the backend storage system where the backup resides (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
| `id` | path | `string` | yes | The unique identifier of the backup to restore from. Must be URL-safe and compatible with filesystem paths (only lowercase, numbers, underscore, minus characters allowed). |
