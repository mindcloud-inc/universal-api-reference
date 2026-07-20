# Create Campaign with SendPulse

Creates a new campaign in SendPulse.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Create Campaign](https://sendpulse.com/integrations/api/bulk-email#create-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the campaign. |
| `subject` | body | `string` | yes | Email subject line. |
| `sender_name` | body | `string` | yes | Display name of the sender. |
| `sender_email` | body | `string` | yes | Verified sender email address. |
| `list_id` | body | `string` | yes | Mailing list used for the campaign. |
| `body` | body | `string` | no | Base64-encoded HTML body for the campaign. Provide this or Template ID. |
| `template_id` | body | `string` | no | Template used to render the campaign. Provide this or HTML Body Base64. |
| `type` | body | `string` | no | Use draft to create safely before scheduling or sending. |
| `send_date` | body | `string` | no | Optional scheduled send date and time. Requires active emails in the mailing list. |
