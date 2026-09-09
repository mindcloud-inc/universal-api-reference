# Delete Campaign with Walmart

Permanently remove an existing Campaign from the system.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v3/advertising/sem/campaigns/:campaignId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Delete Campaign](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign ID of the campaign whose details are to be retrieved. |
