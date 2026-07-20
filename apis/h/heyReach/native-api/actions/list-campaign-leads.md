# List Campaign Leads with Hey Reach

Retrieves leads from a Hey Reach campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/campaign/GetLeadsFromCampaign`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List Campaign Leads](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | body | `number` | yes |
| `offset` | body | `number` | no |
| `limit` | body | `number` | no |
| `timeFrom` | body | `date` | no |
| `timeTo` | body | `date` | no |
| `timeFilter` | body | `string` | no |
