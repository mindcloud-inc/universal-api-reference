# Import Campaign Template with Sarbacane

Adds content to a campaign send in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{campaignId}/send/{sendId}/content`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Import Campaign Template](https://developers.sarbacane.com/campaigns/#add-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | no | Sarbacane campaign ID. |
| `sendId` | path | `string` | no | Sarbacane send ID. |
