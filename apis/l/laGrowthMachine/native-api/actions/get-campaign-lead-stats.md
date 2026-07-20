# Get Campaign Lead Stats with LaGrowthMachine

Retrieves campaign lead stats from LaGrowthMachine.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/statsleads`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Get Campaign Lead Stats](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign ID. |
| `getLeadsAfter` | query | `string` | no | Lead ID cursor for the next page. |
| `getLeadsBefore` | query | `string` | no | Lead ID cursor for the previous page. |
