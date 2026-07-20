# Create Ingest Job with Agentset

Creates an ingest job in an Agentset namespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/ingest-jobs`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Create Ingest Job](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
| `payload` | body | `object` | yes | The ingest payload to submit. |
