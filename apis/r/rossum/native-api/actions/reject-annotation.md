# Reject Annotation with Rossum

Rejects an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/reject`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Reject Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `note_content` | body | `string` | no | Optional rejection note. |
| `automatically_rejected` | body | `boolean` | no | Mark the rejection as automatic in Rossum statistics. |
