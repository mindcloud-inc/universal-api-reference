# List Tag Assignments with Nozbe Personal

Retrieves accessible tag assignments from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag_assignments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Tag Assignments](https://api4.nozbe.com/v1/api#/tag_assignments/getTagAssignments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Return assignments for this task. |
| `tag_id` | query | `string` | no | Return assignments for this tag. |
| `fields` | query | `string` | no | — |
