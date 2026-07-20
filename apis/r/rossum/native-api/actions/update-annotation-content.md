# Update Annotation Content with Rossum

Updates annotation content in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/annotations/:annotationID/content`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Annotation Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `content` | body | `list<object>` | yes | Rossum partial annotation content payload. |
