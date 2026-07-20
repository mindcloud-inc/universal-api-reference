# Find Queues For Source with FutureAGI

## Endpoint

- **Method:** `GET`
- **Path:** `/model-hub/annotation-queues/for-source/`
- **Base URL:** `https://api.futureagi.com`
- **Official documentation:** [Find Queues For Source](https://docs.futureagi.com/docs/api/annotations/queues/find-queues-for-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | query | `string` | no | Source UUID. |
| `source_type` | query | `string` | no | Source type, for example trace, span, generation, or session. |
