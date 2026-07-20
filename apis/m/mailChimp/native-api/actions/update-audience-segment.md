# Update Audience Segment with Mailchimp

Updates an existing segment in a Mailchimp audience.

## Endpoint

- **Method:** `PATCH`
- **Path:** `lists/:list_id/segments/:segment_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update Audience Segment](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `name` | body | `string` | yes | Segment name. |
| `options` | body | `object` | no | Segment options object. |
| `segment_id` | path | `string` | yes | The unique ID for the audience segment. |
| `static_segment[]` | body | `array<string>` | no | Static segment member list. |
| `options.match` | body | `list<string>` | no | Match type for segment conditions (any or all). Accepted values: `all`, `any`. |
| `options.conditions[]` | body | `array<object>` | no | Array of segment condition objects. |
