# Get Campaign with Mailchimp

Retrieves a campaign from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `campaigns/:campaign_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Campaign](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `include_resend_shortcut_eligibility` | query | `boolean` | no | — |
| `include_resend_shortcut_usage` | query | `boolean` | no | — |
