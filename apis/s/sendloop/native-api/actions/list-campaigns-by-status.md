# List Campaigns by Status with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign.getlistbystatus/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [List Campaigns by Status](https://chmyos.notion.site/Get-Campaign-List-By-Status-a6c63b9183544388994012eb22ad0e94)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignStatus` | body | `string` | yes | Target campaign status: Draft, Scheduled, Outbox, or Sent |
| `Limit` | body | `number` | no | Number of records to return |
| `Page` | body | `number` | no | Page number to return |
| `OrderByField` | body | `string` | no | Sort field: CampaignID, CampaignName, or SendTime |
| `OrderBySort` | body | `string` | no | Sort direction: ASC or DESC |
| `TargetListID` | body | `number` | no | If provided, only campaigns sent to this list are returned |
