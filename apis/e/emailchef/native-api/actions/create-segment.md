# Create Segment with Emailchef

Creates a new segment in Emailchef.

## Endpoint

- **Method:** `POST`
- **Path:** `segments`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Create Segment](https://emailchef.com/integration/#/Segments/createSegment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `instance_in.list_id` | body | `string` | yes |
| `instance_in.logic` | body | `string` | yes |
| `instance_in.condition_groups[]` | body | `array<object>` | yes |
| `instance_in.name` | body | `string` | yes |
| `instance_in.description` | body | `string` | no |
| `instance_in.condition_groups[].logic` | body | `string` | no |
| `instance_in.condition_groups[].conditions[].field_id` | body | `string` | no |
| `instance_in.condition_groups[].conditions[].name` | body | `string` | no |
| `instance_in.condition_groups[].conditions[].comparable_id` | body | `string` | no |
| `instance_in.condition_groups[].conditions[].comparator_id` | body | `string` | no |
| `instance_in.condition_groups[].conditions[].value` | body | `string` | no |
