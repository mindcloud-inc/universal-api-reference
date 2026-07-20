# Assign Annotation with Rossum

Assigns assignees to an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/assign`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Assign Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotations[]` | body | `array<string>` | yes | Annotation URLs to assign. |
| `assignees[]` | body | `array<string>` | yes | User URLs to assign to the annotation. |
| `note_content` | body | `string` | no | Optional reassignment note. |
