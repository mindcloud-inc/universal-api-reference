# Update Email Campaign with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/emailCampaigns/:campaignId`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Email Campaign](https://developers.brevo.com/reference/update-email-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Email campaign ID. |
| `subject` | body | `string` | no | Updated subject line for the campaign. |
