# Update Scheduled Campaign with SendPulse

Updates a scheduled campaign in SendPulse.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/:campaignId`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Update Scheduled Campaign](https://sendpulse.com/integrations/api/bulk-email#edit-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The SendPulse campaign identifier. |
| `name` | body | `string` | no | Updated campaign name. |
| `subject` | body | `string` | no | Updated email subject line. |
| `sender_name` | body | `string` | no | Updated sender display name. |
| `sender_email` | body | `string` | no | Updated sender email address. |
| `body` | body | `string` | no | Updated base64-encoded HTML body for the campaign. |
| `list_id` | body | `string` | no | Updated mailing list for the campaign. |
| `template_id` | body | `string` | no | Updated template identifier. |
| `send_date` | body | `string` | no | Scheduled send date and time. |
