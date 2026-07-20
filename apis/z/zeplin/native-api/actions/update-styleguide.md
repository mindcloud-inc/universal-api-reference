# Update Styleguide with Zeplin

Updates an existing styleguide in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide](https://docs.zeplin.dev/reference/updatestyleguide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `name` | body | `string` | yes | New name for the styleguide |
| `description` | body | `string` | yes | New description for the styleguide |
| `linked_parent_styleguide_id` | body | `string` | yes | The unique id of the styleguide to be linked as parent. Set null to unlink the linked parent styleguide. |
