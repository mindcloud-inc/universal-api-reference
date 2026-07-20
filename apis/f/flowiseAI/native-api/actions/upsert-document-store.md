# Upsert Document Store with FlowiseAI

Upserts documents in a FlowiseAI document store.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-store/upsert/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Upsert Document Store](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented document store upsert fields. |
| `id` | path | `string` | yes | Document store ID for upsert. |
