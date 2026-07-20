# Create Custom Activity Definition with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/definitions/activity/create`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Create Custom Activity Definition](https://help.ortto.com/a-273-create-a-custom-activity-definition-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Custom activity definition name. |
| `icon_id` | body | `string` | no | Ortto icon ID shown for the activity. |
| `track_conversion_value` | body | `boolean` | no | Whether the activity tracks conversion value. |
| `touch` | body | `boolean` | no | Whether the activity updates first seen and last seen. |
| `filterable` | body | `boolean` | no | Whether the activity can be used in filters and reports. |
| `visible_in_feeds` | body | `boolean` | no | Whether the activity is shown in feeds. |
| `display_style` | body | `object` | yes | Display style object with type and optional title or attribute references. |
| `attributes[]` | body | `array<object>` | yes | Array of custom activity attribute definitions. |
