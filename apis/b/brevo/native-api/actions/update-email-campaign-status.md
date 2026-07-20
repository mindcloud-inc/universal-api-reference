# Update Email Campaign Status with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/emailCampaigns/:campaignId/status`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Email Campaign Status](https://developers.brevo.com/reference/updatecampaignstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The email campaign identifier. |
| `status` | body | `string` | yes | The new campaign status. |
