# Create View with SmartSuite

Creates a new view in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Create View](https://developers.smartsuite.com/docs/solution-data/views/create-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application` | body | `string` | yes | The SmartSuite table ID the view belongs to. |
| `solution` | body | `string` | yes | The SmartSuite solution ID containing the table. |
| `label` | body | `string` | yes | The label shown for the new SmartSuite view. |
| `view_mode` | body | `string` | yes | The SmartSuite view mode, such as grid. |
| `state` | body | `object` | yes | The SmartSuite view state object, including visible fields and filter settings. |
| `order` | body | `number` | no | Optional ordering value for the view. |
| `description` | body | `string` | no | Optional description for the view. |
| `autosave` | body | `boolean` | no | Whether the SmartSuite view autosaves changes. |
| `is_dirty` | body | `boolean` | no | Internal SmartSuite dirty-state flag for the view. |
| `is_locked` | body | `boolean` | no | Whether the SmartSuite view is locked. |
| `is_password_protected` | body | `boolean` | no | Whether the SmartSuite view is password protected. |
| `is_private` | body | `boolean` | no | Whether the SmartSuite view is private. |
| `map_state` | body | `object` | no | Map configuration state for map views. |
| `sharing_allow_all_fields` | body | `boolean` | no | Whether shared views expose all fields. |
| `sharing_allow_copy` | body | `boolean` | no | Whether shared views allow copying. |
| `sharing_allow_export` | body | `boolean` | no | Whether shared views allow export. |
| `sharing_allow_open_records` | body | `boolean` | no | Whether shared views allow opening records. |
| `sharing_enabled` | body | `boolean` | no | Whether sharing is enabled for the view. |
| `sharing_hash` | body | `string` | no | Optional SmartSuite sharing hash. |
| `sharing_password` | body | `string` | no | Optional password for the shared view. |
| `sharing_show_toolbar` | body | `boolean` | no | Whether shared views show the toolbar. |
