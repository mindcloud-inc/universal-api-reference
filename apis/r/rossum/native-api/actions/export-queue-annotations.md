# Export Queue Annotations with Rossum

Exports annotations from a Rossum queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/queues/:id/export`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Export Queue Annotations](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Queue ID to export annotations from. |
| `status` | query | `string` | no | Annotation status filter for the export. |
