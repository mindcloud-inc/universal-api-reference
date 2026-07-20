# Send Draft Campaign with Campaign Monitor

Sends a draft campaign in Campaign Monitor.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/send.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Send Draft Campaign](https://www.campaignmonitor.com/api/v3-3/campaigns/#sending-draft-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign Monitor campaign identifier. |
| `ConfirmationEmail` | body | `string` | yes | Email address to receive the send confirmation. |
| `SendDate` | body | `string` | yes | Date and time to send the campaign, or Immediately. |
