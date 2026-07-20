# Delete an email from a campaign with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/campaigns/{campaignId}/{campaignEmailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete an email from a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `campaignEmailId` | path | `string` | yes | ID of the email associated with the campaign |
