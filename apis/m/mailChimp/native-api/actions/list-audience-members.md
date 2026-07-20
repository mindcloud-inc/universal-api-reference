# List Audience Members with Mailchimp

Retrieves members from a Mailchimp audience.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/members`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Audience Members](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_last_changed` | query | `string` | no | — |
| `before_timestamp_opt` | query | `string` | no | — |
| `email_type` | query | `string` | no | — |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `interest_category_id` | query | `string` | no | — |
| `interest_ids` | query | `string` | no | — |
| `interest_match` | query | `string` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `since_last_campaign` | query | `boolean` | no | — |
| `since_last_changed` | query | `string` | no | — |
| `since_timestamp_opt` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `unique_email_id` | query | `string` | no | — |
| `unsubscribed_since` | query | `string` | no | — |
| `vip_only` | query | `boolean` | no | — |
