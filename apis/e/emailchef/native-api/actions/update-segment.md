# Update Segment with Emailchef

Updates an existing segment in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `segments/:segment_id`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Update Segment](https://emailchef.com/integration/#/Segments/updateSegment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segment_id` | path | `string` | yes | The Emailchef segment ID. |
| `instance_in.name` | body | `string` | no | — |
| `instance_in.description` | body | `string` | no | — |
| `instance_in.list_id` | body | `string` | no | — |
| `instance_in.logic` | body | `string` | no | — |
| `instance_in.condition_groups[].logic` | body | `string` | no | — |
| `instance_in.condition_groups[].conditions[].field_id` | body | `string` | no | — |
| `instance_in.condition_groups[].conditions[].name` | body | `string` | no | — |
| `instance_in.condition_groups[].conditions[].comparator_id` | body | `string` | no | — |
| `instance_in.condition_groups[].conditions[].value` | body | `string` | no | — |
