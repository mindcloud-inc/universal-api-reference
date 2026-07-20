# Get Segment Details with Zoho Campaigns

Retrieves segment details from Zoho Campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/getsegmentdetails`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Get Segment Details](https://www.zoho.com/campaigns/help/developers/get-segment-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | List key that owns the target segment. |
| `cvid` | query | `string` | yes | Segment ID (`cvid`) to inspect. |
