# Get an email by ID for a specific campaign with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaigns/{campaignId}/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get an email by ID for a specific campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `emailId` | path | `string` | yes | ID of the email |
