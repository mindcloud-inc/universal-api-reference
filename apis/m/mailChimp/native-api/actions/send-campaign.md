# Send Campaign with Mailchimp

Sends a campaign from Mailchimp.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns/:campaign_id/actions/send`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Send Campaign](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Actions/Send.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
