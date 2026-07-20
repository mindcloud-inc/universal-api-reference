# Create Annotation Queue with Langfuse

Creates an annotation queue in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotation-queues`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Annotation Queue](https://api.reference.langfuse.com/#tag/AnnotationQueues/POST/api/public/annotation-queues)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `name` | body | `string` | no |
| `scoreConfigIds` | body | `string` | no |
