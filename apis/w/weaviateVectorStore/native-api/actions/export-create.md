# Start a new export with Weaviate Vector Store

Starts a new export in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/export/:backend`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Start a new export](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | The backend storage system to use for the export (e.g., `filesystem`, `gcs`, `s3`, `azure`). |
