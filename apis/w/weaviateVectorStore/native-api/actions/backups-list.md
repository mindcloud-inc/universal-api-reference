# List all created backups with Weaviate Vector Store

Retrieves all created backups from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/backups/:backend`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [List all created backups](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | Specifies the backend storage system to list backups from (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
| `order` | query | `string` | no | Order of returned list of backups based on creation time. (asc or desc) |
