# Reorder emails in a campaign with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaignId}/reorder`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Reorder emails in a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `emails[]` | body | `array<string>` | yes | Send multiple values as a array. |
