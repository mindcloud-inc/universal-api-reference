# Update Annotation Queue Item with Langfuse

Updates an item in a Langfuse annotation queue.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/annotation-queues/:queueId/items/:itemId`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Update Annotation Queue Item](https://api.reference.langfuse.com/#tag/AnnotationQueues/PATCH/api/public/annotation-queues/{queueId}/items/{itemId})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | path | `string` | no |
| `queueId` | path | `string` | no |
| `status` | body | `string` | no |
