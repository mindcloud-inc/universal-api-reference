# Re-Ingest Job with Agentset

Starts re-ingestion for an Agentset ingest job.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/ingest-jobs/:jobId/re-ingest`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Re-Ingest Job](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/re-ingest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The ingest job ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
