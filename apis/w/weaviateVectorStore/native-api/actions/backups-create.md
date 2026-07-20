# Create a backup with Weaviate Vector Store

Creates a backup in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/backups/:backend`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Create a backup](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | Specifies the backend storage system where the backup will be stored (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
