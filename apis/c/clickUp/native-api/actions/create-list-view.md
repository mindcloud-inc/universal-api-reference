# Create List View with ClickUp

Creates a new view for a ClickUp List.

## Endpoint

- **Method:** `POST`
- **Path:** `list/:list_id/view`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create List View](https://developer.clickup.com/reference/createlist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `columns.fields[]` | body | `array` | yes |
| `divide.collapsed[]` | body | `array<string>` | no |
| `filters.op` | body | `string` | yes |
| `grouping.field` | body | `string` | yes |
| `sorting.fields[]` | body | `array` | yes |
| `filters.fields[]` | body | `array<object>` | yes |
| `grouping.dir` | body | `number` | yes |
| `filters.search` | body | `string` | no |
| `grouping.collapsed[]` | body | `array<string>` | no |
| `type` | body | `string` | yes |
| `filters.show_closed` | body | `boolean` | yes |
| `grouping` | body | `object` | yes |
| `grouping.ignore` | body | `boolean` | no |
| `divide` | body | `object` | yes |
| `sorting` | body | `object` | yes |
| `filters` | body | `object` | yes |
| `columns` | body | `object` | yes |
| `team_sidebar` | body | `object` | yes |
| `settings` | body | `object` | yes |
