# List Templates with Mailchimp

Retrieves templates from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `templates`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Templates](https://us22.api.mailchimp.com/schema/3.0/Paths/Templates/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `before_date_created` | query | `string` | no |
| `category` | query | `string` | no |
| `content_type` | query | `string` | no |
| `created_by` | query | `string` | no |
| `exclude_fields` | query | `string` | no |
| `fields` | query | `string` | no |
| `folder_id` | query | `string` | no |
| `since_date_created` | query | `string` | no |
| `type` | query | `string` | no |
