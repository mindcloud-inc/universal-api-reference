# Confirm Annotation with Rossum

Confirms an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/confirm`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Confirm Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `skip_workflows` | body | `boolean` | no | Whether to skip workflow evaluation when confirming. |
