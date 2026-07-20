# Stop Lead In Campaign with Hey Reach

Stops a lead in a Hey Reach campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/campaign/StopLeadInCampaign`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Stop Lead In Campaign](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | body | `number` | yes |
| `leadMemberId` | body | `string` | no |
| `leadUrl` | body | `string` | no |
