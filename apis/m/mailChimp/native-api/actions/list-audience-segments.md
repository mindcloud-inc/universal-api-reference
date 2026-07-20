# List Audience Segments with Mailchimp

Retrieves segments from a Mailchimp audience.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/segments`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Audience Segments](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_created_at` | query | `string` | no | — |
| `before_updated_at` | query | `string` | no | — |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `include_cleaned` | query | `boolean` | no | — |
| `include_transactional` | query | `boolean` | no | — |
| `include_unsubscribed` | query | `boolean` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `since_created_at` | query | `string` | no | — |
| `since_updated_at` | query | `string` | no | — |
| `type` | query | `string` | no | — |
