# List Annotation Queue Items with Langfuse

Retrieves items from a Langfuse annotation queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/annotation-queues/:queueId/items`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Annotation Queue Items](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues/{queueId}/items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `queueId` | path | `string` | no |
| `status` | query | `string` | no |
