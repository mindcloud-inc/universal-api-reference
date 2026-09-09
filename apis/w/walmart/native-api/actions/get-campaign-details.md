# Get Campaign Details with Walmart

Retrieve detailed information about a specific Campaign. Provide the Campaign's unique ID in the request to fetch its attributes.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/advertising/sem/campaigns/:campaignId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Campaign Details](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign ID of the campaign whose details are to be retrieved. |
