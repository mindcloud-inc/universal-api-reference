# List Campaigns with LaGrowthMachine

Retrieves campaigns from LaGrowthMachine.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [List Campaigns](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | yes | Maximum number of campaigns to return. |
| `skip` | query | `number` | yes | Number of records to skip for pagination. |
