# Get Campaign Report with Mailchimp

Retrieves a campaign report from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `reports/:campaign_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Campaign Report](https://us22.api.mailchimp.com/schema/3.0/Paths/Reports/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
