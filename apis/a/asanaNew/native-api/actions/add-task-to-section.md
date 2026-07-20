# Add task to section with Asana

Adds a task to a section in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `sections/:section_gid/addTask`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add task to section](https://developers.asana.com/reference/addtaskforsection)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.insert_after` | body | `string` | yes |
| `data.insert_before` | body | `string` | yes |
| `data.task` | body | `string` | yes |
| `section_gid` | path | `string` | yes |
