# Retrieve Ingest Job with Agentset

Retrieves an ingest job from Agentset by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId/ingest-jobs/:jobId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Retrieve Ingest Job](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The ingest job ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
