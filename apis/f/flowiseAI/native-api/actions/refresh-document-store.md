# Refresh Document Store with FlowiseAI

Reprocesses all documents in a FlowiseAI document store.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-store/refresh/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Refresh Document Store](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented document store refresh fields. |
| `id` | path | `string` | yes | Document store ID for refresh. |
