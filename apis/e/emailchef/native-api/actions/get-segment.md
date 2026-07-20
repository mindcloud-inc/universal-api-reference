# Get Segment with Emailchef

Retrieves a segment from Emailchef.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/segments/:segment_id`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Get Segment](https://emailchef.com/integration/#/Segments/getSegment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The Emailchef list ID. |
| `segment_id` | path | `string` | yes | The Emailchef segment ID. |
