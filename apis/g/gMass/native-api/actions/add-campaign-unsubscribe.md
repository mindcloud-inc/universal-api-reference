# Add Campaign Unsubscribe with GMass

Suppresses an email address for a GMass campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/unsubscribes/:campaignId`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Add Campaign Unsubscribe](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_AddUnsubscribeForCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | GMass campaign ID to suppress the address for. |
| `emailAddress` | body | `string` | yes | Email address to suppress for the selected campaign. |
