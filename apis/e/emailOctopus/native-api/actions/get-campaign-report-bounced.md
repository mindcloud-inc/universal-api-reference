# Get Campaign Report: Bounced with EmailOctopus

Retrieves the bounced report for an EmailOctopus campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/report/bounced`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Get Campaign Report: Bounced](https://emailoctopus.com/api-documentation/campaigns/report/get-bounced)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The unique ID of the campaign. |
