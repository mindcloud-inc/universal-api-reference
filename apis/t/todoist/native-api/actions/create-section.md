# Create Section with Todoist

Creates a new section in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sections`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Create Section](https://developer.todoist.com/api/v1/#tag/Sections/operation/create_section_api_v1_sections_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Section name. |
| `project_id` | body | `string` | yes | Project ID where the section will be created. |
| `order` | body | `number` | no | Custom section order value. |
