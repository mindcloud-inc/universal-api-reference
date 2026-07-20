# Cancel an export with Weaviate Vector Store

Cancels an export in Weaviate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/export/:backend/:id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Cancel an export](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backend` | path | `string` | yes | The backend storage system where the export is stored. |
| `id` | path | `string` | yes | The unique identifier of the export to cancel. |
