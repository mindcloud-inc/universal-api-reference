# Copy Annotation with Rossum

Copies an annotation to another Rossum queue.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/copy`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Copy Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `annotationID` | path | `number` | yes |
| `target_queue` | body | `string` | yes |
| `target_status` | body | `string` | no |
| `reimport` | query | `boolean` | no |
