# List Merge Fields with Mailchimp

Retrieves merge fields from a Mailchimp audience.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/merge-fields`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Merge Fields](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/MergeFields/Collection.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `required` | query | `boolean` | no | — |
| `type` | query | `string` | no | — |
