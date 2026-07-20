# Create Annotation Queue Item with Langfuse

Adds an item to a Langfuse annotation queue.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotation-queues/:queueId/items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Annotation Queue Item](https://api.reference.langfuse.com/#tag/AnnotationQueues/POST/api/public/annotation-queues/{queueId}/items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `objectId` | body | `string` | no |
| `objectType` | body | `string` | no |
| `queueId` | path | `string` | no |
| `status` | body | `string` | no |
