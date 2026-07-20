# Update Course Module with Mentortools

Updates an existing course module in Mentortools.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/v1/modules/:module_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Update Course Module](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_id` | path | `number` | yes | The module ID. |
| `title` | body | `string` | yes | Title of the module. |
| `order` | body | `number` | yes | Order of the module. |
| `is_active` | body | `boolean` | no | Whether the module is active. |
| `is_published` | body | `boolean` | no | Whether the module is published. |
| `mandatory` | body | `boolean` | no | Whether the module is mandatory. |
