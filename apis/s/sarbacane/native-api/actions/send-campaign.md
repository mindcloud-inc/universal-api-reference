# Send Campaign with Sarbacane

Sends an existing campaign in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{campaignId}/send`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Send Campaign](https://developers.sarbacane.com/campaigns/#send-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | no | Sarbacane campaign ID. |
| `requestedSendDate` | body | `string` | no | ISO timestamp for the requested send date. |
