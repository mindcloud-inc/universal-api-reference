# Update Document Store with FlowiseAI

Updates an existing document store in FlowiseAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/document-store/store/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Update Document Store](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented document store fields to update. |
| `id` | path | `string` | yes | Document store ID to update. |
