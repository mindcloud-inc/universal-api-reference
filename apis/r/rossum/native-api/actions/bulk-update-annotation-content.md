# Bulk Update Annotation Content with Rossum

Updates annotation content in bulk in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/content/operations`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Bulk Update Annotation Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `operations` | body | `list<object>` | yes | Rossum bulk content operations payload. |
