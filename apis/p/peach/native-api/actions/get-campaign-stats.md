# Get Campaign Stats with Peach

Retrieves campaign performance statistics from Peach.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/stats/:accountId/:campaignId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Get Campaign Stats](https://peach-organization.gitbook.io/peach/api-reference/campaigns/get-campaign-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The Peach account ID for the campaign owner. |
| `campaignId` | path | `string` | yes | The unique identifier of the campaign. |
