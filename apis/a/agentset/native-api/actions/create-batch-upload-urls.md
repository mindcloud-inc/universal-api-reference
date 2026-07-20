# Create Batch Upload URLs with Agentset

Creates presigned batch file upload URLs in Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/uploads/batch`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Create Batch Upload URLs](https://docs.agentset.ai/api-reference/endpoint/uploads/batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<object>` | yes | The files to create upload URLs for. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
