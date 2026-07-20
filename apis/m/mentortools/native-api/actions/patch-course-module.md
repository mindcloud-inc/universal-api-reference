# Patch Course Module with Mentortools

Updates part of an existing course module in Mentortools.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/modules/:module_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Course Module](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_id` | path | `number` | yes | The module ID. |
| `title` | body | `string` | no | Title of the module. |
