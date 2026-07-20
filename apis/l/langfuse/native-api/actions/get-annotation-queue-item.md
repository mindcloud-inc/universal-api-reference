# Get Annotation Queue Item with Langfuse

Retrieves an item from a Langfuse annotation queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/annotation-queues/:queueId/items/:itemId`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Get Annotation Queue Item](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues/{queueId}/items/{itemId})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | path | `string` | no |
| `queueId` | path | `string` | no |
