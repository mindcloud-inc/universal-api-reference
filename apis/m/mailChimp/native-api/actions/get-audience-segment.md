# Get Audience Segment with Mailchimp

Retrieves a segment from a Mailchimp audience.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/segments/:segment_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Audience Segment](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `include_cleaned` | query | `boolean` | no | — |
| `include_transactional` | query | `boolean` | no | — |
| `include_unsubscribed` | query | `boolean` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `segment_id` | path | `string` | yes | The unique ID for the audience segment. |
