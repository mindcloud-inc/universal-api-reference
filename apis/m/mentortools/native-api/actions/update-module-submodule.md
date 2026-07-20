# Update Module Submodule with Mentortools

Updates an existing submodule in Mentortools.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/v1/submodules/:submodule_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Update Module Submodule](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submodule_id` | path | `number` | yes | The submodule ID. |
| `order` | body | `number` | yes | — |
| `title` | body | `string` | yes | — |
| `is_published` | body | `boolean` | no | — |
