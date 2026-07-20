# View Time Summary Analytics for a bulk send out - campaign with Routee

Retrieves time summary analytics for a bulk send out - campaign from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/breakdown/perCampaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Time Summary Analytics for a bulk send out - campaign](https://docs.routee.net/reference/view-time-summary-analytics-for-a-bulk-send-out)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | query | `string` | yes | The Id of the campaign |
| `offset` | query | `date` | yes | The time offset that the result will be calculated in ISO 8601. |
