# Patch Module Submodule with Mentortools

Updates part of an existing submodule in Mentortools.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/submodules/:submodule_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Module Submodule](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submodule_id` | path | `number` | yes | The submodule ID. |
| `order` | body | `number` | no | — |
| `title` | body | `string` | no | — |
| `is_published` | body | `boolean` | no | — |
