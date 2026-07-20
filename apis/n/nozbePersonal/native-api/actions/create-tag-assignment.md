# Create Tag Assignment with Nozbe Personal

Creates a new tag assignment in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/tag_assignments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Tag Assignment](https://api4.nozbe.com/v1/api#/tag_assignments/postTagAssignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | body | `string` | yes | Tag to assign. |
| `task_id` | body | `string` | yes | Task that receives the tag. |
