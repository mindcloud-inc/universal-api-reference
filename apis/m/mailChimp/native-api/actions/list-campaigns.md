# List Campaigns with Mailchimp

Retrieves campaigns from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `campaigns`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Campaigns](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_create_time` | query | `date` | no | Only include campaigns created before this ISO 8601 datetime. |
| `before_send_time` | query | `date` | no | Only include campaigns sent before this ISO 8601 datetime. |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `folder_id` | query | `string` | no | Filter campaigns by folder id. |
| `include_resend_shortcut_eligibility` | query | `boolean` | no | Include resend shortcut eligibility in campaign response. |
| `list_id` | query | `string` | no | Filter campaigns by audience/list id. |
| `member_id` | query | `string` | no | Filter campaigns sent to a specific member hash. |
| `since_create_time` | query | `date` | no | Only include campaigns created after this ISO 8601 datetime. |
| `since_send_time` | query | `date` | no | Only include campaigns sent after this ISO 8601 datetime. |
| `status` | query | `list<string>` | no | Filter campaigns by status. Accepted values: `paused`, `save`, `schedule`, `sending`, `sent`. |
| `type` | query | `list<string>` | no | Filter campaigns by type. Accepted values: `absplit`, `plaintext`, `regular`, `rss`, `variate`. |
