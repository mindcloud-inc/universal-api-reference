# Export Annotations Cross-Queue with Rossum

Exports annotations across Rossum queues.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/export`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Export Annotations Cross-Queue](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotations[]` | body | `array<string>` | yes | Annotation URLs to export across queues. |
