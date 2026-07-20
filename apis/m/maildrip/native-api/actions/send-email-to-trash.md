# Send email to trash with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaigns/{campaign_id}/{campaign_email_id}/send-mail-to-trash`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send email to trash](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign |
| `campaign_email_id` | path | `string` | yes | ID of the email to be sent to trash |
