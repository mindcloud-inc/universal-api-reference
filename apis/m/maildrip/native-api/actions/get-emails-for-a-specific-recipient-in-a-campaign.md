# Get emails for a specific recipient in a campaign with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaignId}/recipient-emails`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get emails for a specific recipient in a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `recipientEmail` | body | `string` | yes | — |
