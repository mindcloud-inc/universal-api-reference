# List Reports with Mailchimp

Retrieves campaign reports from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `reports`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Reports](https://us22.api.mailchimp.com/schema/3.0/Paths/Reports/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `before_send_time` | query | `string` | no |
| `exclude_fields` | query | `string` | no |
| `fields` | query | `string` | no |
| `since_send_time` | query | `string` | no |
| `type` | query | `string` | no |
