# Get Audience with Mailchimp

Retrieves an audience from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Audience](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `include_total_contacts` | query | `boolean` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
