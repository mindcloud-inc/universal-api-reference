# Update Annotation with Rossum

Updates an annotation in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/annotations/:annotationID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `metadata.mindcloud_test_marker` | body | `string` | yes | Metadata marker for safe runtime validation. |
