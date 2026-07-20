# Modify Custom Activity Definition with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/definitions/activity/modify`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Modify Custom Activity Definition](https://help.ortto.com/a-274-modify-a-custom-activity-definition-modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity_field_id` | body | `string` | yes | Custom activity field ID to modify. |
| `name` | body | `string` | no | Updated custom activity definition name. |
| `state` | body | `string` | no | Activity state such as live. |
| `icon_id` | body | `string` | no | Ortto icon ID shown for the activity. |
| `track_conversion_value` | body | `boolean` | no | Whether the activity tracks conversion value. |
| `touch` | body | `boolean` | no | Whether the activity updates first seen and last seen. |
| `filterable` | body | `boolean` | no | Whether the activity can be used in filters and reports. |
| `visible_in_feeds` | body | `boolean` | no | Whether the activity is shown in feeds. |
| `display_style` | body | `object` | no | Display style object with type and optional title or attribute references. |
| `attributes[]` | body | `array<object>` | no | Array of custom activity attribute definitions. |
