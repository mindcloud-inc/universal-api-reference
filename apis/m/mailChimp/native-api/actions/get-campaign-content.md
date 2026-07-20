# Get Campaign Content with Mailchimp

Retrieves campaign content from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `campaigns/:campaign_id/content`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Campaign Content](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Content/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
