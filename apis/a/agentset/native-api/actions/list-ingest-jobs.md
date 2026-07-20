# List Ingest Jobs with Agentset

Retrieves ingest jobs from an Agentset namespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId/ingest-jobs`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [List Ingest Jobs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
