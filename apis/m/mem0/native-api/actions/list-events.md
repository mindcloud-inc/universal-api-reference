# List Events with Mem0

Retrieves events from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [List Events](https://docs.mem0.ai/api-reference/events/get-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for Mem0 events list pagination. |
| `page_size` | query | `number` | no | Page size for Mem0 events list pagination. |
| `org_id` | query | `string` | no | Mem0 organization ID filter for events when supported. |
| `project_id` | query | `string` | no | Mem0 project ID filter for events when supported. |
