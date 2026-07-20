# Get Email Campaign Activity with Constant Contact

Retrieves an email campaign activity from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails/activities/:campaign_activity_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Get Email Campaign Activity](https://developer.constantcontact.com/api_guide/email_campaigns_activity_id.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_activity_id` | path | `string` | yes | The unique ID for an email campaign activity. |
| `include` | query | `string` | no | Comma-separated additional fields to include. |
