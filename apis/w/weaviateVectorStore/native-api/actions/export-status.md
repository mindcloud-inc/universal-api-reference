# Get export status with Weaviate Vector Store

Retrieves export status from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/:backend/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get export status](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | The backend storage system where the export is stored. |
| `id` | path | `string` | yes | The unique identifier of the export. |
