# Add Audience Segment with Mailchimp

Creates a new segment in a Mailchimp audience.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/segments`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Add Audience Segment](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Collection.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `name` | body | `string` | yes | Segment name. |
| `options` | body | `object` | no | Segment options object. |
| `static_segment[]` | body | `array<string>` | no | Static segment member list. |
| `options.match` | body | `list<string>` | no | Match type for segment conditions (any or all). Accepted values: `all`, `any`. |
| `options.conditions[]` | body | `array<object>` | no | Array of segment condition objects. |
