# List Audiences with Mailchimp

Retrieves audiences from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `lists`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Audiences](https://mailchimp.com/developer/marketing/api/lists/get-lists-info/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated fields to include in the response. Send multiple values as a array. |
| `exclude_fields` | query | `string` | no | Comma-separated fields to exclude from the response. |
| `before_date_created` | query | `date` | no | Return audiences created before this ISO-8601 datetime. |
| `since_date_created` | query | `date` | no | Return audiences created after this ISO-8601 datetime. |
| `before_campaign_last_sent` | query | `date` | no | Return audiences with last campaign sent before this ISO-8601 datetime. |
| `since_campaign_last_sent` | query | `date` | no | Return audiences with last campaign sent after this ISO-8601 datetime. |
| `email` | query | `string` | no | Restrict results to audiences containing this subscriber email. |
| `has_ecommerce_store` | query | `boolean` | no | Only include audiences connected to an active ecommerce store. |
| `include_total_contacts` | query | `boolean` | no | Include approximate total contact counts in stats. |
