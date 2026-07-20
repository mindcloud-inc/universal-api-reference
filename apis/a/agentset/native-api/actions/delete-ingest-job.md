# Delete Ingest Job with Agentset

Deletes an ingest job from Agentset.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/namespace/:namespaceId/ingest-jobs/:jobId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Delete Ingest Job](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The ingest job ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
