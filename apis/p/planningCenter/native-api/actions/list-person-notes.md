# List Person Notes with Planning Center

Retrieves notes for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/notes`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Person Notes](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/note)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person_id` | path | `string` | yes |
| `include` | query | `string` | no |
| `order` | query | `string` | no |
| `where[note]` | query | `string` | no |
| `where[note_category_id]` | query | `string` | no |
