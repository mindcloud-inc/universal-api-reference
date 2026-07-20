# List Member Tags with Mailchimp

Retrieves tags for a member from a Mailchimp audience.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/members/:subscriber_hash/tags`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Member Tags](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Tags.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | path | `string` | yes | MD5 hash of the lowercase subscriber email address. |
